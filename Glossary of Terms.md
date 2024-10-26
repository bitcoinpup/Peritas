### Glossary of Terms

**AES-256 Encryption**: Advanced Encryption Standard (AES) with a 256-bit key size, used within Peritas to secure local data storage and cloud backups, ensuring user data remains private and protected against unauthorized access.

**Base Key**: The initial keypair generated on app startup, foundational for deriving other keys (e.g., Social Recovery Keys, Vault Keys) and enabling recovery configurations.

**BIP-85**: A Bitcoin Improvement Proposal used to generate child keys deterministically from a master seed. In Peritas, BIP-85 may be used to create child keys (e.g., Social Recovery Keys) from the Base Key, ensuring compatibility and ease of recovery.

**Bitcoin**: A decentralized digital currency operating on a peer-to-peer network without a central authority. Bitcoin supports self-custody options like single-signature and multi-signature wallets for secure fund management.

**Cloud Backup**: An optional, encrypted storage solution using third-party cloud services (e.g., iCloud, Google Drive) that enhances redundancy for key material, allowing users to recover their keys in the event of device loss.

**Configuration Files**: Files within the Peritas app that contain essential wallet settings, helping manage vault structures and other key parameters. These differ from descriptor files, which specifically outline multi-signature requirements.

**Descriptor Files**: Files that define the spending and access conditions for multi-sig wallets in the Peritas app, ensuring the multi-sig configuration’s integrity by preventing unauthorized modifications.

**Encryption**: The process of encoding information to prevent unauthorized access, commonly used in Peritas through AES-256 encryption to secure both local and cloud-stored data.

**Founder / Vault Founder**: The user who creates a multi-sig vault within Peritas. The Founder is responsible for determining the multi-sig setup and selecting trusted contacts or third-party Keyholders.

**Keyholder**: A trusted contact selected by the Vault Founder who holds a Social Recovery Key. Keyholders can provide recovery assistance in case the Founder loses access to their primary keys.

**Multi-Factor Authentication (MFA)**: An added security layer within Peritas that requires users to verify their identity using multiple forms of authentication before accessing their account, protecting against unauthorized access.

**Multi-Signature (Multi-Sig) Wallet**: A Bitcoin wallet that requires multiple keys to authorize a transaction. Multi-sig wallets enhance security by distributing custody across multiple signatories, reducing single points of failure.

**Nostr Gift-Wrapped Messages**: A secure communication protocol option used within Peritas for transmitting public keys, descriptors, and signatures, providing privacy during inter-user communications.

**Pears Integration**: An additional secure communication protocol under consideration in Peritas for transmitting keys and signatures, enhancing the security of public key exchanges.

**Pro Mode**: An advanced setup option within Peritas, allowing users to customize signatories beyond the default 2/3 multi-sig configuration and access more complex multi-sig wallet structures.

**Public Key Transmission**: The process of securely transferring public keys (using protocols like Nostr Gift-Wrapped Messages or Pears integration) between the Vault Founder and Keyholders, maintaining confidentiality during multi-sig setup.

**Self-Custody**: The practice of managing and securing one’s own Bitcoin keys without relying on third-party custodians. Peritas supports self-custody by providing an accessible multi-sig setup that doesn’t require external hardware.

**Social Recovery Key**: A key created by a Keyholder and shared with the Vault Founder to be included in the multi-sig configuration. This key enables social recovery, supporting account recovery efforts if needed.

**Threshold**: The minimum number of keys required to authorize a transaction in a multi-sig wallet. Peritas allows the Vault Founder to customize this threshold during the vault setup, enabling tailored security levels.

**Third-Party Keyholder**: An optional third-party (e.g., exchange, Bitcoin support service) integrated into the Peritas vault structure to provide technical support and assist with complex multi-sig setups. Third-Party Keyholders may reduce privacy in exchange for added support.

**Tor Integration**: An optional privacy feature within Peritas that allows users to connect to Bitcoin nodes anonymously, masking their IP address to prevent tracking and maintain user privacy.

**Vault**: A multi-sig wallet created by the Vault Founder within Peritas, using multiple keys to enhance security and enable recovery mechanisms through Keyholders or third-party services.

**Vault Key**: A private key derived from the Base Key, specifically for use within the multi-sig vault. Vault Keys are unique to each vault and are securely stored within the app’s encrypted data.

**Web of Trust (WOT)**: A security model that uses social trust networks to verify identities and strengthen authentication, employed by Peritas to foster trusted interactions between Founders, Keyholders, and other collaborators.