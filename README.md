graph LR
A[Start: Enrol patients meeting criteria] --> B{Yes}
B --> C{Daily Data Collection}
C --> D{Demographics}
C --> E{Clinical Information}
C --> F{Hospital Course}
C --> G{Medication Use}
G --> G1{Antimicrobials}
G --> G2{Other Drugs & Fluids}
C --> H{Antimicrobial Classification (ATC)}
H --> I{Prescribing Quality Evaluation}
I --> J{Use PQI Questionnaire (22 questions)}
J --> K{Answer using References}
K --> L{Evaluate Drug Interactions}
G1 --> M{Is brand name?}
M(yes) --> N{Look up cost (CIMS, MIMS, IDR)}
M(no) --> O{Check hospital pharmacy cost}
O,N --> P{Calculate Drug Cost}
C --> Q{Patient Follow-up (Interview/Call)}
Q --> R{Medication Adherence}
Q --> S{Adverse Drug Reactions}
Q --> T{Treatment Response}
P,R,S,T --> U{Calculate PQI Score}
U --> V{Interpret PQI Score (Quality)}
V --> W(End)
B(no) --> C
A --> X[No: Discharged?]
X(yes) --> W
X(no) --> B
