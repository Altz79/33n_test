[![33N](https://github.com/Altz79/33n_test/actions/workflows/new_app.yml/badge.svg)](https://github.com/Altz79/33n_test/actions/workflows/new_app.yml)

## Solution for adding extra column on the events table representing the most recent diagnosis after that event.

###### Output
File "events_with_diagnosis.csv" has data from "Events" combined by EventID with diagnosis information from "Diagnosis" dataset. 
Additionally two new columns are present to flag potentially incorrect data, which could be quickly filtered out in Tableu:
- events where diagnosis data is older than date of an event (value "True" for column "Diagnosis_date_before_event") 
- events with no ID (value "True" for column "No_event_id")

###### Testing
Done with GitHub Actions.

###### Next steps 
Discuss with viz developers team:
- in "Events" dataset we have identical IDs with different PatientID, which now will receive the same diagnosis from "Diagnosis" table. It may be incorrect. Important question - can we have "PatientID" column in "Diagnosis"? Another option is to remove duplicated EventID from the final output to make data more reliable.
