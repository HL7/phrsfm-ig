### Introduction

In 2011, the presence of mobile devices became a highly discussed topic in the health care marketplace. The PHR WG felt it important to include some dialogue that is occurring in the industry. As this dialogue matures, functions and criteria will be developed in the PHR-S FM to support the relationship between Mobile Devices and PHRs.

### PHR Relationship to Mobile Devices

Access to PHR data using new technology such as mobile devices needs to be considered for the near future. Since mobile devices are widely used in society today it is not uncommon to expect access to healthcare data to be available via such devices. In fact, many providers are using tablet computers, cell phones, and smart phones to access healthcare data today or to review their patients’ data. Healthcare professionals, consumers, allied providers, and other emerging groups within the healthcare industry will need to use mobile devices to access healthcare information.

In recognition of this medical device and mobile application access need, the PHR WG has attempted to anticipate emerging technologies, architectures (such as portal, tethered, and non-tethered HIE organizations), and other needs (such as future genetic information-sharing requirements).

### Trustworthiness of Mobile Device Information Sources

Providers and other health care professionals need to be able to verify and trust the source of information that is rendered on a mobile device. All data should display its source. Anything displayed should be customizable to the user (e.g., human languages, reading level, and usability).

The PHR Functional Model has indicators which help to resolve these questions by audit measures in recording that data has been accessed, and by whom. In addition, the PHR records if any user changes data which is professionally sourced data. In short the information stored on the PHR-S has anticipated these concerns.

### Possibility of Consumer Alteration of Professionally-sourced Data

Providers and other health care professionals need to be able to determine whether a consumer has altered professionally-sourced data that is rendered on a mobile device.

### Possibility of Other Alterations of Professionally-sourced Data

Providers and other health care professionals need to be able to determine whether other, non-consumer alterations have been made to professionally-sourced data that is rendered on a mobile device. For example, a computer application may summarize or blend certain information together before sending it to a mobile device; that computer application may have introduced anomalies into the resulting information. Also, data may be rendered differently in one geographic location versus another. For example, a date may be rendered MMDDYYYY in one area, but DDMMYYYY in another.

### Possibility of Insufficient/Unexpected Governance or Management of Professionally-sourced Data

Providers and other health care professionals need to be able to determine whether information quality and/or integrity have suffered due to data governance or data management issues. For example, a professional may establish a rule that delivers an alert to the provider when certain abnormal health conditions appear in a patient, but the mobile device application that governs or manages that alert may behave in an unexpected manner (for example, blocking the alert-message or translating the alert into a device-vibration-request (unaware that the vibration mode has been switched off).

The PHR systems functional model will denote alteration of data has occurred through the audit function (who has accessed the record) and a data element denoting a change to the record.

### Interoperability Standardization within Health Information Exchange Environments

Health data may be stored and exchanged across a variety of systems (e.g., patient system, provider, or other source (such as a Health Information Exchange). Standards-based information exchange (even to the data-element level) is crucial to the successful interchange and utility of data in such an environment.

Standards may need to be modified from time to time to adapt to the ever-changing landscape of systems that manage the PHR data over a lifetime.

### Various Types of Mobile Devices

Mobile devices can be categorized according to the range of their capabilities. For example, a “Dumb Mobile Device” would store electronic Protected Health Information on a remote system, not on the device. A “Smart Mobile Device” could collect information that is manually entered by the user; perhaps collect information from nearby electronic devices; perhaps store some of that information on the handheld device; perhaps amalgamate or integrate (e.g., summarize) sets of information; perhaps transmit some data to an external system; perhaps integrate with an external application(s).

The PHR data must preserve the data it receives and audit what happens to the data over time. The PHR should also indicate the source for receipt of data and the modem of receipt.

Example: The consumer (source) entering their diabetes results via diabetic monitor device (modem).

### Functionality (or capability) –Nuances of Various Information Exchange Systems

The healthcare professional might not be aware of the dynamic adjustments that have been made regarding the “pipeline” or “data-channel” that is used to render information on a mobile device. For example, one mobile device may have a finer-grained display than another display, causing the same image to be displayed differently on each mobile device. Use-ability considerations impacted by external issues and technology of the rendering device need to be accessed and determined acceptable for application within a mobile devices.

### Labeling of Mobile Devices (and corresponding software) as “Regulated” by the FDA

Healthcare professionals need to be aware of the presence (or absence) of a “regulated” label on mobile devices. For example, one electronic bathroom scale may be regulated by a federal organization (for recording the weight of a patient who is under the care of a cardiac surgeon); another bathroom scale may not be regulated (for recording daily weight). Regulatory review and approval and/or all such agency approval for quality measures and standard approvals should be indicated on any device used for healthcare purposes.

### Amount or Type of Data

The “amount of data” or the “type of data” could be a factor that prevents providers and other health care delivery professionals from using mobile devices. For example, the information that arrives on a provider’s mobile device might need to be summarized, filtered, staged, translated (for example, into an alert message), or merged with other data before being sent to the mobile device. Sometimes the source-information is sparse; sometimes it is so very plentiful that it is best summarized (or graphed, for example). Since it may be important for the user of the mobile device to be aware of any transformations that were applied to information being rendered on a mobile device, the system should provide the ability to display information that describes any transformations that were made to the data. Consequently, the system should be sensitive to the need to provide the ability to identify “pre-transformation” data.

Another issue is the configuration of the parameters that control mobile device information delivery and/or display: Users (providers and consumers) of mobile devices have varying needs for information and data exchange. Data configuration by user (e.g. amount, type, granularity, timing, level-of-urgency, frequency, mode, etc. and type of data) either received or sent via a mobile device will be needed.

### Future Vision

Future Power of PHR systems - Use of Mobile Devices for Clinical Decision Support:

Any mobile device application that is intended to run on a mobile device platform and that is also used to provide Clinical Decision Support services, may be subject to jurisdictional regulations.

For example, in the U.S. different agencies regulate mobile applications and security:
* The Food and Drug Administration (FDA) regulates medical devices and mobile applications related to patient safety. For example, the FDA regulates a small subset of mobile medical applications that may present a potential risk to patients if those devices do not work as intended.
* The Federal Communications Commission (FCC) regulates interstate and international communications by wire, satellite and cable related to mobile devices. For example, the FCC regulates certain Radio Frequency (RF) -based medical devices, including implanted devices (e.g., heart pacemakers) and patient monitoring devices (e.g., wireless telemetry devices).
* The Federal Trade Commission (FTC) protects consumers from unfair business practices. For example, the FTC enforces a rule requiring certain entities to notify consumers when there has been a breach involving their electronic health information.
* The National Institute of Standards and Technology (NIST) promotes innovation and industrial competitiveness by advancing measurement science and standards. For example, the Information Technology Laboratory is charged with helping to insure the security of technology used in federal information systems.
* Office of Civil Rights (OCR) Department of Health and Human Services (DHHS) is responsible for implementing and supporting HIPAA (“ensures the privacy, integrity, and availability of electronic protected health information through standards for administrative, physical, and technical safeguards”) 
* States in the U.S. also have different jurisdictional priorities and processes regarding security and privacy of health information.
Responsibility for regulating medical and mobile technologies may cross two or more regulatory structures with subsequent relationships developed between two or more agencies. The agencies would then collaborate through informal communication, or possibly, a more formal means, such as the execution of a Memorandum of Understanding. These relationships between agencies allow for a concerted effort to provide regulatory predictability, consistency, and swiftness to the market and safety for the consumer when developing public policy to address emerging technologies.

### Location of Data-At-Rest

It is likely that sensitive information (also known as Protected Health Information) may reside on mobile devices and may not be secure. The data on the mobile device may need to be offered security and privacy protection services. The consumer should be informed that consenting to extract data from a secure system and passing it through a mobile device application service (for display on a mobile device), might increase the risks to that data’s security and privacy.

Certain Protected Health Information might be collected from time to time on a consumer’s mobile device and stored for specified duration before being routed to a secure site. For example, the consumer’s mobile device might collect blood pressure readings once an hour in the patient’s home after cardiac surgery, but only transmit those readings to a secure site at midnight.

Consumers may be responsible for data stored on their mobile devices. Consumers may need to decide whether they continue to store that information on the device or purge the information from the device once data is forwarded. (Such action may be subject to jurisdictional laws or regulations.)

### Management of lost, stolen, or misplaced mobile devices

When a mobile device is lost, stolen, or misplaced, there can be sensitive data on the mobile device. A mechanism for addressing corresponding issues needs to be addressed.

### Consents, Authorizations, and other Governance issues

Mobile devices ought to be able to locate, interrogate, and respect consents (capture and store legal documents), authorizations, preferences (electronic settings within the PHR) and other governance expectations (with respect to sensitive data or certain functionality). The mobile device may be able to allow an updated consent. Examples of governance expectations include mobile device –controlled information exchange, synchronization, management, and/or reconciliation among Personal Health Record (PHR) systems, Electronic Health Record (EHR) systems, or other systems.

### Location Awareness Services

Mobile device users may benefit from Location Awareness Services that identify and respond to changes in geographic and/or jurisdictional boundaries. For example, when visiting a new city the user may need to locate the nearest dialysis machine or methadone clinic. However, consider that even the request for such information may disclose certain health conditions regarding the user.

### Use of multiple mobile devices

Issues arise when multiple mobile devices are used by a given user. For example, issues arise when a physician uses a mobile tablet computer while caring for a certain patient while in the hospital, but then switches to a personal smart phone after leaving the hospital. Systems should be aware of the use of multiple device types available to a user (e.g., personal computer, tablet, and smart phone). System should handle the necessary access security for each device type. Systems should recognize a user’s preference for data delivery on a certain device and should accommodate transitions that may occur throughout the day across multiple devices.

### Usage heuristics

A mobile health solution (platform) could possess functionality that recognizes that the current user is using the mobile device in a manner that is uncharacteristic of the designated owner (possibly revealing theft, fraud, or abuse). For example, a mobile device should not be used to request pregnancy services for an infant, or to request insurance coverage for medicines not prescribed for the owner. (This functionality is similar to that used by credit card services.)

### Difference Between “Patient-entered” and “Patient- sourced’ Data

Is there a difference between “patient-entered” and “patient-sourced” data? If so, what impact might these two types of data have on the users of such data (specifically, on providers who view such information on mobile devices)? For example, what does “patient-entered” data mean when the number “165” appears as the patient’s weight for last Tuesday? Did the data come from a reading made by the patient while standing on a bathroom scale – or was it an estimate made by looking in the mirror? Was the scale recently calibrated? Was the scale’s spring cold (yielding a high number)? Was the patient lying (or being overly optimistic about the number), that is, the scale displayed 185 but the patient refused to believe the number? Was the patient wearing heavy boots and a coat? Did the patient transpose the numbers during data-entry, i.e., from “156”? Was the battery low, yielding an inaccurate reading?

Or did the number come from a smart-bathroom-scale-device that electronically transmits the identity of the machine, the date/time, and the patient’s weight to a mobile device (that sends a packet of data to the patient’s computer, whereby the patient eventually forwards that packet to a PHR system). Perhaps the receiver is a smart-phone that contains an “App-For-That” that collects the electronic packet and automatically routes it to the patient’s PHR system.

So the questions are: Who (or what) entered the data? And who (or what) is the source? And, could that data be “bad” for some reason (e.g., misleading, incorrect, or imprecise)?

Furthermore, if a patient’s mobile device receives a laboratory report from a laboratory via a “Direct-To-Consumer” laboratory service – and the patient forwards that document into his PHR, is that data considered to be professionally-sourced or patient-sourced?
Therefore, though it is important for the professional to know the source of a piece of data being displayed on a mobile device, it may be very difficult to determine the actual source of the data. Questions arise regarding: author-of-the-data, source-of-the-data (such as a smart-bathroom-scale), type-of-transmission-method, and intermediary-processing (such as merging multiple records into a time-graph, or summarizing multiple records).

Sometimes an organizational entity may be considered as the originator (i.e., the source) of the health care data (for example, the city water department). It could be that who (or what) enters the data into the PHR is considered to be the author of the data. In some cases the source and the author may be the same.

### Difference Between “Author-of-the-data” and “Source-of-the data”

The author of the data may be a consumer entering their weight on a daily basis according to the scale (the source) into the PHR. If there is a “smart bathroom scale”, the scale may be capable of uploading information directly to the PHR; in that case the bathroom scale might be considered to be both the source and the author of the data.

### Relationships between PHR, EHR, and Mobile Devices

Medical Devices collect health information about an individual which may be exported to a Personal Health Record (PHR) system, Electronic Health Record (EHR) system, or another system. Depending on the purpose and capabilities of a given mobile device, the device may be able to share its data with these systems in various formats, ranging from raw (unformatted) data, to coded / mapped values, to fully summarized and formatted reports. Furthermore, the systems may need to collect the data from the mobile device in multiple formats to adequate support users in various roles who might use the PHR data. For example, someone in the role of a patient who has diabetes may use a PHR system to see a summary report from a blood pressure device that states, “Your blood pressure is very high today. Contact your physician immediately.” Someone in the role of a provider (while using an EHR system) may require raw blood pressure data values from the past two weeks. The same mobile device may generate glucose values that are of interest to the patient’s nutritionist. These values may be combined with values from other mobile devices to create synthesized reports that are richer in content and value than those reports resulting from devices whose information cannot be synthesized. This level of power requires that the PHR system interact with mobile devices in sophisticated ways, including: the ability to configure the mobile device data input according to granularity, type, format, frequency, etc. of data collected; the ability to code or map data; the ability to summarize, filter, or merge data; the ability to route data to pre-designated role-types; the ability to tailor the data according to role-types; the ability to transform the data into alerts or notifications. As the PHR system’s ability to manage mobile device data increases, so does the value of the mobile device data – and of the PHR system itself. Mobile device –related gains made by the PHR system can, and should, be shared with EHR (and other) systems.

### Responses to Rules-engine Requests

A personal healthcare device (or other data capture device) ought to be able to respond to a rules-engine -based request from a Personal Health Record (PHR) system, Electronic Health Record (EHR) system, or other system – so that those systems can tailor their interactions with the mobile device. More specifically, the mobile device ought to be able to negotiate with other systems so that it can integrate its capabilities (or lack of capabilities) with those of other systems. For example, if the patient’s weight has increased more than two percent during the previous week, then the EHR system could recommend that the PHR system request blood pressure reports once an hour from a mobile device, rather than once a day. The mobile device should be able to declare its ability to comply with the updated data-collection expectation.

### Security and Privacy Obligations Vary Between Providers and Consumers

Consumers must rely upon the providers’ adherence to standards and regulations to insure that proper levels of security and privacy are maintained (with respect to protected health information (PHI) held by providers). In the case of PHI held by consumers (such as in a Personal Health Record system or on the consumer’s mobile device), the same security and privacy regulations may not apply. Instead the consumer should be able to manage access to the mobile device – and applications on that device that constitutes a compensating control. The objective is to enable the consumer to specify a level of consent for access to their PHR that balances ease-of-access to critical information versus protection of private information in accordance with any applicable jurisdictional law of that may apply.