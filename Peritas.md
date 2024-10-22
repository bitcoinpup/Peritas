# **Peritas: An Accessible Multi-Signature Wallet Solution for Enhanced Self-Custody**

## **Abstract**

Peritas aims to provide a simple, open-source, multi-platform application designed to simplify the setup and management of multi-signature (multi-sig) wallets. The application specifically targets new Bitcoin users, enhancing the security of their holdings without requiring additional hardware. By creating an accessible, intuitive interface and aligning with Web of Trust (WOT) principles, Peritas addresses a significant gap in the Bitcoin ecosystem, promoting higher security with minimal user friction.

## **1. Introduction**

Bitcoin wallets typically take one of two forms: single-signature (single-sig) and multi-signature (multi-sig). Single-sig wallets are the default, and they are most commonly used by those new to self-custody as they are simple to set up and manage. However, single-sig wallets present a security risk as only one key is needed to access and move funds, leaving them vulnerable to theft or compromise.

Multi-sig wallets require multiple keys to authorize transactions, significantly enhancing security by distributing custody across multiple signatories. Multi-sig should be the standard for all Bitcoin self-custody setups, particularly for key recovery and backup processes, as an improvement over traditional paper seed backups.

This white paper proposes Peritas: an open-source, multi-platform application that simplifies multi-sig wallet creation and operation, making enhanced security accessible to all Bitcoin users without the need for dedicated hardware.

## **2. System Overview**

### 2.1 Wallet Creation Process

Peritas provides users with a simple, guided process for creating a secure multi-sig wallet:

- Users begin by selecting the option to create a new "vault" (multi-signature wallet). The default configuration is a 2/3 multi-sig setup, although users can access advanced settings to adjust the number of signatories and the threshold required for authorizing transactions.
- The application generates a new Bitcoin key, securely encrypting it on the user’s device as a software key.
- It is important to tailor multi-sig setups to the user’s situation, skill level, and the size of their holdings. For smaller amounts (e.g., 100,000 sats), a **2/3 service-based multi-sig** involving keys held on the user’s phone, a spouse’s or trusted contact's device, and the exchange where one purchases Bitcoin or a vetted third-party key holder may be appropriate, providing a balance of convenience and security. For larger holdings, users may opt for a more secure configuration with a higher number of signatories and a higher threshold for transaction authorization to enhance protection and mitigate risks.

### 2.2 Integration with Trusted Contacts

- Users are prompted to select a trusted contact who can generate a "Social Recovery Key." The public key from this newly generated keypair, created through a simple option on the app’s welcome page, is shared back with the user for use in the configuration of their multi-sig vault.
- An "affiliate + key assistance" system may also be used, where the additional key could be managed by the person who onboarded the user (e.g., a mentor or trusted friend), reinforcing usability and trust.

### 2.3 Third-Party Collaborative Custody

- Peritas offers flexibility for the third key in the multi-sig setup. While users can choose to partner with an exchange, they may also select a vetted partner of their choice. Peritas will build partnerships with respected Bitcoin support and mentorship services that offer third-party key custody as a service. These vetted partners may charge a fee for advanced support or assistance if required.
- Alternatively, if the user prefers, they can choose another trusted contact to create a second Social Recovery Key, allowing for a more private Vault configuration.

### 2.4 Vault Creation and Management

- With the user’s, trusted contact’s, and third-party public keys in place, Peritas creates a multi-signature vault and shares descriptor files securely with the trusted contact and the exchange.
- The app houses configuration files for each multi-sig wallet and enforces security by **rejecting any attempt to add additional keys from the same multi-sig setup**, ensuring that a quorum of keys cannot be consolidated on a single device.

### 2.5 Encrypted Cloud Backup

- To enhance redundancy, Peritas offers users the option to encrypt and store their key material in their preferred cloud service (e.g., iCloud, Google Drive). This approach leverages familiar systems providing a seamless way for users to store recovery keys.
- This minimizes the risk of loss of key material in the event of device loss or app data deletion.

## **3. Technical Implementation**

### 3.1 Security Architecture

- **Encryption**: All communication between the app, users, trusted contacts, and exchanges is encrypted using AES-256 and other state-of-the-art encryption protocols to ensure privacy and prevent interception or tampering.
- **Cross-Platform Support**: Peritas is designed to function across multiple platforms (iOS, Android, Windows, Linux) to ensure broad accessibility.
- **Public Key Transmission**: Secure communication protocols such as Fedi, Matrix, or Nostr Gift-Wrapped Messages may be used to transmit public keys, descriptor files, and signatures, safeguarding user information.

### 3.2 User Experience Design

- **Onboarding and Education**: A setup wizard guides users through wallet creation, using simple language and visual aids to explain multi-sig benefits, vault concepts, and the roles of trusted contacts and exchanges.
- **Customization**: Users can access an advanced “Pro Mode” for configuring signatories beyond the default 2/3 setup, allowing for custom thresholds and advanced wallet configurations.

### 3.3 Node Connectivity

To maintain decentralization and minimize the risk associated with a single point of failure, Peritas will not rely on a central node for its operations. Instead, the application will offer multiple options for users:

- **Custom Node Connections**: Users can connect Peritas to their own Bitcoin nodes, providing maximum control and security. This approach aligns with the Bitcoin ethos of self-sovereignty and reduces reliance on third-party infrastructure.
- **Public Node Selection**: For users without their own nodes, the application will provide a selection of vetted, community-operated public nodes to connect with. This offers convenience while distributing trust across multiple independent entities, minimizing the risk of centralization.
- **Tor Integration**: To enhance privacy, Peritas will support Tor integration, enabling users to connect to nodes anonymously and reducing the risk of tracking and monitoring.
- **Automatic Node Load Balancing**: The app may implement a feature that automatically rotates between multiple trusted public nodes, ensuring that no single node becomes a point of dependency.

## **4. Security and Privacy Considerations**

Peritas prioritizes security and privacy:

- **Multi-Factor Authentication (MFA)**: To protect app access, users may set up MFA as an additional security layer.
- **Local and Cloud Encryption Standards**: The app uses AES-256 for local storage of keys and end-to-end encryption for cloud backups and transmission of public keys and descriptors.
- **Key Recovery and Redundancy**: Cloud services are employed for encrypted backups, providing redundancy while ensuring that users retain control over their key material.

## **5. Integration and Collaboration Opportunities**

### 5.1 Wallet Providers

- Peritas could partner with existing open-source wallet providers, such as Nunchuk, to integrate its multi-sig functionality and expand their security offerings.

### 5.2 Exchange Collaboration

- By collaborating with exchanges, Peritas can provide seamless integration for obtaining Exchange Public Keys, building trust and simplifying the user experience for those securing their funds.

## **6. Future Development and Monetization**

### 6.1 Feature Expansion

- **Hardware Wallet Integration**: Future updates will include compatibility with hardware wallets, providing additional security options for advanced users who wish to incorporate dedicated signing devices into their multi-sig setup.
- **Automatic Backup Options**: Users will have more automated and secure options for backing up their encrypted keys, including automated cloud backups and integration with secure storage solutions.
- **Transaction Monitoring**: The app will incorporate transaction monitoring services, enabling users to receive alerts and detailed information about incoming and outgoing transactions.
- **Guided Key Rotation/Replacement**: To maintain long-term security and minimize risks from potential key compromises, Peritas will offer a guided process for rotating or replacing keys within a multi-sig setup. The feature will provide users with step-by-step instructions on how to update their vault’s keys, ensuring a secure and seamless transition without risking access to funds.

### 6.2 Premium Services

- Potential premium services advanced support for users configuring complex multi-sig setups. These services may be facilitated through strategic partnerships with community-vetted organizations such as **Bitcoin Mentor** or **The Bitcoin Way**, ensuring trusted and expert guidance for users.

## **7. Market Considerations and Demand**

While specialized hardware signing devices will continue to cater to those with heightened security demands (i.e., “paranoid crypto anarchists”), Peritas fills a gap for new entrants to the space who may not yet be ready or willing to purchase dedicated hardware. Providing robust, easy-to-use software solutions ensures that the demand for secure self-custody is met for all levels of users.

## **8. Conclusion**

Peritas is a critical step forward in improving Bitcoin self-custody security. By offering an open-source, user-friendly application for multi-signature wallet setup and management, Peritas empowers users to protect their holdings without the need for additional hardware. Every self-custody setup should incorporate multi-sig, and Peritas provides an adaptable, secure solution to meet this need, ensuring that new users have access to robust security models that align with the ethos of Bitcoin’s financial sovereignty. **By paving a path to accessible and secure Bitcoin self-custody for the coming waves of new Bitcoin participants, Peritas aims to uphold and strengthen the principles of financial freedom and autonomy in the Bitcoin ecosystem.**

## **9. Contributors and Acknowledgements**

Peritas was developed with insights and support from several key contributors in the Bitcoin community:

- **Guy Swann**, founder of Bitcoin Audible, provided valuable perspectives on multi-signature setups and emphasized the importance of using multi-sig as the standard for Bitcoin self-custody and recovery processes.
- We also acknowledge the efforts of the many **builders and developers** who have worked tirelessly to bring Bitcoin self-custody to its present stage, creating the tools and upholding the principles that Peritas hopes to further.
- Additional input and feedback were provided by members of the Bitcoin community who share a commitment to enhancing security and accessibility for Bitcoin newcomers.
