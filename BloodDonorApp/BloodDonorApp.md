# BloodDonorApp Data Protection Impact Assessment (DPIA)

| Student | Contribution | Blood Group | Rh Factor |
|-|-|-|-|
| Stefan Ohnewith  | "Consideration about collection", "Conclusion" sections | 0 | positive |
| Ernst Schwaiger  | "Description of Blood Donor App", "References" sections | 0 | positive |
| Nermin Topalovic | "Description of Blood Donor App", "References" sections | A | positive |

## Brief Description of the Blood Donor App Project and Data Processing Goals

The Austrian Red Cross conducts blood donations, stores, and distributes blood units to institutions which administer blood to patients.
Currently, prospect donors have to fill out a paper questionnaire which is evaluated by a doctor before being admitted to donate blood. The questionnaire contains roughly 40 questions, among others, regarding the prospect donors past and present health, regarding surgical procedures, and sexual activities, see [Blutspendedienst_Fragebogen.pdf](https://www.roteskreuz.at/fileadmin/user_upload/LV/VB/Landesverband/Blutspendedienst/Blutspendedienst_Fragebogen.pdf).

When the prospect donor is admitted to donate blood, and the donated blood was administered to a patient, the questionnaire has to be kept by the Red Cross for at least 30 years, according to Austrian Law: Blutsicherheitsgesetz §11 (5).

In order to reduce waiting times for prospect donors, an app shall be implemented in which an appointment with the Red Cross venue can be arranged. Moreover the app shall allow the user to fill out the questionnaire upfront and send it to the venue along with the agreed appointment data to a dedicated Server. The doctor can then print out and evaluate the questionnaire, and on the doctors discretion, admit the donor to the donation.

As the app allows the blood donor to interrupt the filling out of the questionnaire, the already answered questions have to be stored on the cell phone in such a way that they can't be read by a another person without consent of the donor. Once the filled out questionnaire arrives at the server, care must be taken that no unauthorized personnel can access that data.

After a successful donation, and if the blood actually got administered to a patient, a Record of that questionnaire must be kept for 30 years according to the Austrian Law.

Austrian law regulates how blood donations are to be conducted in the [Blutspendeverordnung](https://www.jusline.at/gesetz/bsv)(BSV) and in the [Blutsicherheitsgesetz](https://www.jusline.at/gesetz/bsg)(BSG).

>Blutsicherheitsgesetz §11 (5): 
>(5)Die Dokumentation ist durch mindestens fünfzehn Jahre - jene Teile, die für die lückenlose Nachvollziehbarkeit der Transfusionskette unerlässlich sind durch mindestens dreißig Jahre - zur jederzeitigen Einsichtnahme durch die nach diesem Bundesgesetz zuständigen Kontrollorgane bereitzuhalten.

The process of blood donation is roughly as follows: A prospect donor uses the BloodDonorApp to arrange an appointment the Red Cross venue and to fill out the questionnaire. Both appointment and questionnaire are transmitted to a Server maintained by the Red Cross (1).

At the appointment date, the prospect donor visits the site, where the transmitted questionnaire can be printed out to a paper form (2). The heart rate, blood pressure and the hemoglobin level (and, unless already provided in a blood donor card, the blood group and Rhesus factor) of the prospect donor are taken  and written down in the paper form.

<p align="center">
  <img src="Workflow.drawio.png" alt="Workflow.drawio.png">
</p>

If the measured values are within the required boundaries, the donor then visits a doctor who checks the questionnaire and asks the prospect donor additional health related questions. Also, the prospect donor may ask questions, e.g. related to the blood donation process. If the doctor comes to the conclusion that the prospect donor is fit enough and the questionnaire did not reveal any issues preventing a donation, the prospect donor is admitted to the blood donation process (4), otherwise the prospect donor cannot donate blood in the moment and is asked to visit the venue in a few weeks e.g. after enough time after a recently suffered cold has elapsed (3).

During the donation process, additional blood samples are taken for the screening of the blood; the samples are, for instance, checked for HIV, Hepatitis B/C.

If the samples did not reveal any problems, the donated blood can then be delivered to health institutions in need and eventually administered to a patient. The filled questionnaire, together with the lab results of the blood samples are then sent to a long term data storage for at least 30 years as required by Austrian legislation (5).

## Consideration about collection, use, disclosure and storage of personal data

- **Description of the personal data**
  - Name and contact details
  - Date of birth
  - Appointment data
  - Questionnaire answers
  - Health data
  - Medical measurements
  - Laboratory test results
  - Donation and traceability data

- **Key privacy elements: purpose for which personal data is collected, processed, disclosed**
  - Personal data is collected to organize appointments and assess donor eligibility.
  - Health-related data is processed to protect donor health and ensure the safety of donated blood.
  - Personal data may be disclosed internally to authorized medical staff and, where necessary, to laboratories or supervisory authorities.
  - Personal data is stored to document the donation process and to comply with legal traceability and retention obligations.

- **Nature and sensitivity of the personal data**
  - The project processes sensitive personal data.
  - This includes health data and possibly highly personal data from the questionnaire like medication, allergies, drinking habits, etc.
  - The data requires a high level of confidentiality and protection because unauthorized access could seriously affect the privacy of the donor.

## Conclusion: Is a DPIA necessary?

- **A DPIA is necessary.**
- The project involves the processing of sensitive personal data, especially health data.
- It also includes long-term storage and medical assessment in a structured workflow.
- Therefore, the processing is likely to result in a high risk to the rights and freedoms of the data subjects.
- For that reason, carrying out a DPIA is necessary.

# DPIA

## Description of the process activity
The app allows prospective blood donors to arrange an appointment and fill out the donor questionnaire before visiting the donation venue. The questionnaire and appointment data are transmitted to a server operated by the Red Cross. At the venue, the questionnaire may be printed and reviewed by medical staff. Additional medical measurements are taken on site, including heart rate, blood pressure, hemoglobin level, and, where necessary, blood group and Rhesus factor. A doctor then reviews the questionnaire and decides whether the person may donate blood.
During or after the donation process, blood samples are tested for infections such as HIV and hepatitis B/C. If the blood is suitable and is administered to a patient, the questionnaire, lab results, and traceability-relevant documentation are stored long-term

- **Types and amount of personal data being processed**
  - Personal data includes identification and contact data of the donor (name, 
  address, phone number, e-mail address, date of birth)
  - Appointment data
  - Questionnaire answers (medical conditions, weight, pregnancy, alcohol/drug habits, sexual acitivity)
  - Health records and medical measurements
  - Laboratory test results
  - Donation and traceability data

- **Circumstances of the processing**
  - Personal data is processed before, during, and after the donation process
  - Processing takes place via the mobile app, at the donation venue, and on Red Cross servers
  - Medical staff process the data for donor assessment and donation safety
  - Some information may also be processed in paper form

- **How long the personal data will be retained**
  - Personal data is retained as long as necessary for appointment handling and donor assessment
  - Legally required documentation is retained according to Austrian blood safety law (15 years)
  - Traceability-relevant data may need to be retained for up to 30 years

- **How the personal data will be collected, stored, accessed, shared, and ultimately destroyed**
  - Personal data is collected from the donor via the app and during the on-site examination
  - Personal data is stored on the donor’s device, on Red Cross servers, and partly in paper records
  - Access is limited to authorized medical and administrative personnel
  - Personal data is shared only where necessary for testing, documentation, traceability, and legal compliance
  - Personal data is deleted or destroyed securely once it is no longer required by law or operations 

## Description of  purpose(s):

- **Purposes for which personal data is being processed in relation to the necessity and proportionality of the processing operations**
  - Appointment data is needed for scheduling and managing appointments with donors.
  - Questionnaire answers and health data are needed for the medical staff to evaluate whether a prospective donor is eligible to donate blood and whether the donation is safe for both donor and recipient.
  - Laboratory results and medical measurements are necessary to ensure that donated blood is safe for transfusion and complies with applicable medical standards.
  - Donation and traceability data is needed because full tracability of the blood transfusion chain is required by Austrian Law
  - Personal data is processed and retained to fulfill legal obligations under the Austrian Blutsicherheitsgesetz (BSG) and Blutspendeverordnung (BSV)

- **Details of the legal basis, such as the legitimate interest pursued by the controller**
  - GDPR article 6 (a) consent
  - GDPR article 6 (c) processing legally neccessary due to "Blutsicherheitsgesetz"
  - GDPR article 6 (d) vital interest of another person
  regarding special categories of personal data:
  - GDPR article 9 (2)(a) consent
  - GDPR article 9 (2)(c) vital interest of another person
  - GDPR article 9 (2)(h) purpose within health sector
   - GDPR article 9 (2)(i) reasons of public interest in public health
  related laws
  - Blutsicherheitsgesetz §11 (5)


## Description of of the lawfulness of processing
- transparency towards the subject is achieved by clearly communicating the exact purposes and nature of the processing via the data protection declaration that is shown to the user before the questionnaire
- The gathered data is not used for any other purpose than the ones listed above
- The questionnaire doesn't contain any questions that are not strictly necessary to fullfill legal and medical requirements
- To ensure accuracy of the data, there is a donor review process
- A retention schedule by data category is implemented. Abandoned questionnaire drafts get automatically deleted
- Measures such as encryption, access control and logging are taken to fullfill the requirement of integrity and confidentiality

## Identification of risks to the rights and freedoms of individuals (data subjects)

|**Item**|**Describe source of risk and nature of potential impact on individuals.** Include associated compliance and corporate risks as necessary. |**Likelihood of harm**|**Severity of harm**|**Overall risk**|
|-|-|-|-|-|
|1|Rogue Blood donor sends appointment request to donate blood using a false identity|Possible|Low|Low|
|2|Questionnaire stored in the app is read by unauthorized personnel, e.g. from a stolen or unsupervised cellphone|Almost Certain|Severe|High|
|3|Questionnaire data is stolen/altered while being transferred from the cell phone to the Server|Possible|Severe|High|
|4|Server is compromised by a hacker attack|Possible|Very Severe|Very High|
|5|Server hardware gets stolen|Possible|Very Severe|Very High|
|6|Attacker obtains questionnaire of a prospect blood donor by imposing as the donor|Unlikely|Severe|Medium|
|7|Rogue staff member steals or alters questionnaire data from the server|Remote|Very Severe|High|
|8|Rogue member of app development team adds backdoor to server software|Remote|Very Severe|High|
|9|Malicious Blood donor app sends data to unauthorized personnel|Possible|High|Medium|
|10|Long-term archive is compromised by an external attacker. Since questionnaire data, lab results and traceability data may be stored for up to 30 years, a breach could expose highly sensitive health data of many donors.|Possible|Very Severe|Very High|
|11|Unauthorized internal access to long-term records by staff with excessive privileges. This could lead to disclosure of old questionnaire data, lab results or donation records|Remote|Very Severe|High|

FIXME: Also include attacks on the long term storage?

## Description of measures or methods to mitigate risks, both existing and planned

|**Item**|**Options to reduce or eliminate risk**|**Effect on risk**|**Residual Risk**|
|-|-|-|-|
|1|Blood donor must authenticate at the venue using an official document, e.g. passport, drivers license|Reduced|Low|
|2|Questionnaire is stored encrypted on the device, access to app only via MFA|Reduced|Low|
|3|Questionnaire data is encrypted before transmission to server|Reduced|Low|
|4|**Availability**: Provide multiple servers, use load balancer. **Confidentiality/Integrity**: Put server behind firewall, perform security updates regularly, server implementation according to the Secure Software Development Lifecycle. Questionnaire data is deleted immediately after blood donation process finished, or if the donor did not show up at the appointment|Reduced|Medium|
|5|Server hardware is put in a dedicatd windowless room with security door|Reduced|Low|
|6|Prospect blood donors must authenticate themselves using official documents before the questionnaire is printed out|Reduced|Low|
|7|Access to the questionnaire data is logged; server software does not allow to change questionnaire data|Reduced|Low|
|8|No code change enters the main branch of the repo without code review |Reduced|Medium|
|9|Provide app only via official app repositories. Warn users to download the app elsewhere |Reduced|Low|
|10|Encrypt long-term archive, use strict role-based access control, audit logging, regular penetration tests and secure backup procedures |Reduced|Medium|
|11|Apply least-privilege access, periodic access reviews, logging of all archive access and disciplinary procedures for misuse |Reduced|Low|

## Determination of the residual risks:

See table above. 
FIXME: shall we describe the items in more detail, instead of just in a table?
FIXME: The DFA also contains additional items, like:
- statements regarding necessity, commensurability
- Interview affected persons
- Consultation of Data Protection Officer/DPO

## Necessity and proportionality

The processing of personal data is necessary to organize blood donation appointments, assess donor eligibility, protect donor and recipient safety, and fulfil legal documentation and traceability obligations.

The app reduces waiting times at the donation venue by allowing donors to complete the questionnaire before arrival. However, the processing is limited to data that is necessary for appointment handling, medical assessment, blood safety, and legal documentation.

The questionnaire does not collect data for unrelated purposes. Abandoned questionnaire drafts are deleted automatically after a defined period. Data that is no longer required for the donation process or legal retention obligations is securely deleted or destroyed.

The processing is therefore considered proportionate, provided that data minimization, strict access control, encryption, retention limits, and secure deletion are implemented as described.



## References
- [https://www.jusline.at/gesetz/bsg](https://www.jusline.at/gesetz/bsg)
- [https://www.jusline.at/gesetz/bsv](https://www.jusline.at/gesetz/bsv)
- [https://www.jusline.at/gesetz/bsv/paragraf/3](https://www.jusline.at/gesetz/bsv/paragraf/3)
- [https://www.ris.bka.gv.at/GeltendeFassung.wxe?Abfrage=Bundesnormen&Gesetzesnummer=10011170&FassungVom=2023-04-11](https://www.ris.bka.gv.at/GeltendeFassung.wxe?Abfrage=Bundesnormen&Gesetzesnummer=10011170&FassungVom=2023-04-11)
- [https://www.ris.bka.gv.at/GeltendeFassung.wxe?Abfrage=Bundesnormen&Gesetzesnummer=10011145&FassungVom=2023-05-10](https://www.ris.bka.gv.at/GeltendeFassung.wxe?Abfrage=Bundesnormen&Gesetzesnummer=10011145&FassungVom=2023-05-10)
- https://dsgvo-gesetz.de/art-6-dsgvo/

