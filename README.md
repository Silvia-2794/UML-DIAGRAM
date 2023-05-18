@startuml


class MedicationReminder {
  -patientName: String
  -medicationName: String
  -frequency: String
  -reminderTime: Time

  +setReminder(): void
  +cancelReminder(): void
}

class DailyReminder {
}

class WeeklyReminder {
}

class EmailReminder {
}

class SMSReminder {
}

class PhoneReminder {
}

MedicationReminder <-- DailyReminder
MedicationReminder <-- WeeklyReminder
DailyReminder <|-- EmailReminder
DailyReminder <|-- SMSReminder
WeeklyReminder <|-- PhoneReminder

@enduml
