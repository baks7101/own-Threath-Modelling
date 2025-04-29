flowchart TD
    %% External Entities
    A[Healthcare Providers]
    B[Patients]
    C[TeleHealthCare Hub]
    D[MedTrack Pro]
    E[HealthInsight Portal]

    %% Processes
    P1([1. Patient Record Management])
    P2([2. Appointment Scheduling])
    P3([3. Secure Messaging])
    P4([4. Telehealth Sessions])
    P5([5. Medication Management])
    P6([6. Analytics Dashboard])
    P7([7. Patient Engagement Portal])

    %% Data Stores
    D1[(Patient Records Database)]
    D2[(Appointment Data)]
    D3[(Messages & Logs)]
    D4[(Medication Records)]
    D5[(Logs & Metrics)]

    %% Data Flows
    A --> P1
    A --> P2
    A --> P3
    A --> P5
    A --> P7

    P1 --> D1
    P2 --> D2
    P3 --> D3
    P5 --> D4
    P6 --> D5
    P7 --> D1

    B --> P7
    P7 --> B

    P1 --> C
    P2 --> P4
    P4 --> C
    C --> P6
    D --> P5
    P5 --> P6
    P6 --> E

    D1 --> P6
