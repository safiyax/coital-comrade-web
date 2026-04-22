---
title: "Privacy Policy"
date: 2026-01-28
hidemeta: true
showtoc: false
---

## Privacy Policy

**Effective Date:** January 28, 2026
**Last Updated:** April 22, 2026

Coital Comrade is built around a simple principle: your intimate data belongs to you and your partner, and no one else, including us. This policy explains exactly what we collect, what we cannot see, and why.

---

### What Coital Comrade cannot read

Your encounter history, partner names, display names, and avatars are **end-to-end encrypted**. They are encrypted on your device before they ever reach our servers, using keys that exist only in your iOS Keychain. We have no technical ability to decrypt or read this information. Our server stores opaque ciphertext blobs it cannot interpret.

This is not a policy promise. It is a technical guarantee. The encryption keys never leave your device.

---

### Phone number

To create an account, you register with a phone number. We use Twilio Verify to send you a one-time SMS code to confirm your number. Your phone number is used only for this verification step.

**We do not store your phone number.** After verification, we immediately compute a one-way SHA-256 hash of your number and store only the hash. The hash is used solely to detect duplicate registrations (preventing two accounts from being created for the same number). It cannot be reversed to recover your phone number.

Twilio, our SMS provider, processes your phone number to send the verification code. Twilio's privacy policy governs their handling of that data.

---

### Username

You choose a username when you set up your account. Your username is stored in plaintext on our servers. It is visible to other Coital Comrade users and is used to find you when a partner sends a connection request.

---

### Encrypted profile

Your display name and profile photo are stored on our servers as an AES-256-GCM encrypted blob. We cannot read them. The key that encrypts your profile lives only in your iOS Keychain and is shared directly with your partner through the encrypted sync channel, never sent to our server.

---

### Partner relationships

We store the fact that two usernames have a partner relationship, along with its status (pending, active, or blocked) and whether both users have verified their safety numbers in person. We do not store the content of any communications or encounter data associated with that relationship.

---

### Encrypted sync payloads

When you sync encounter data with a partner, your app encrypts the data using the **Signal Protocol** (X3DH key exchange + Double Ratchet). The resulting ciphertext is uploaded to our server as an opaque blob. We store it temporarily so your partner's device can download it. We cannot read, analyze, or share the contents.

Sync payloads are deleted from our servers once both parties have confirmed receipt. The maximum size of a single payload is 1 MB.

---

### What our server knows

To be precise about what we can see:

- That a given phone number hash has an account (not the number itself)
- Your username
- Which usernames are in a partner relationship with each other, and that relationship's status
- When syncs happen and approximately how large the payloads are
- Standard server access logs (IP addresses, request timestamps) retained briefly for security and operational purposes

---

### What our server never sees

- Your phone number
- Your display name or avatar
- Your encounter history, notes, or any other intimate data
- Your profile encryption key
- Any private cryptographic key material

---

### Safety numbers

Coital Comrade displays a 60-digit safety number screen that you and your partner can compare in person to confirm your connection has not been intercepted. This fingerprint is derived on your device from both users' public identity keys using an iterated SHA-512 algorithm. Our server plays no role in computing or verifying safety numbers.

---

### Data you control

- **Delete your account:** Deleting your account removes your username, hashed phone number, public keys, and encrypted profile from our servers. Encounter data on your device is under your control.
- **Uninstalling the app** removes all locally stored data from your device.
- **Your partner's copy** of synced encounters is on their device and is not affected by your account deletion.

---

### Third-party services

We use **Twilio** to send SMS verification codes during registration. Twilio receives your phone number for the purpose of delivering the code. We do not use any analytics, advertising, or tracking services.

---

### Changes to this policy

If we change our data practices, we will update the effective date of this policy and note the changes clearly. Our core commitment, that encounter data is end-to-end encrypted and we cannot read it, is fundamental to how the app is built and will not change without a corresponding technical change that we would describe in detail.

---

### Contact

If you have any questions about this Privacy Policy, please contact us at [me@safiya.sh](mailto:me@safiya.sh).
