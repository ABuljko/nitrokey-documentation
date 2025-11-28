Nitrokey FIDO2 FAQ
==================

.. faq:: Which Operating Systems are supported?

   Windows, Linux, and Mac OS X. Also some support (FIDO2) for Android.

.. faq:: What can I use the Nitrokey for?

   See the `overview <https://www.nitrokey.com/products/nitrokeys>`_ of supported use cases.

.. faq:: What happens if I lose my FIDO device?

   When securing accounts using FIDO (two-factor authentication and
   passwordless login), you should configure another factor in your account as
   a backup. Depending on the service this backup factor can be a phone number,
   an app or even a second Nitrokey FIDO2. If you lose a Nitrokey FIDO2, you
   can still log in with the second Nitrokey FIDO2 (or with another second
   factor).

.. faq:: How large is the storage capacity?

   The Nitrokey FIDO2 doesn't contain storage capability for ordinary data (it can only store cryptographic keys).

.. faq:: How many keys can my Nitrokey FIDO2 store?

   It can store up to 50 passkeys also known as discoverable credentials and an unlimited number of non-discoverable credentials.

.. faq:: How to use Nitrokey FIDO2 with Azure Entra ID (Active Directory)?

   After `disabling Enforce Attestation <https://learn.microsoft.com/en-us/azure/active-directory/authentication/howto-authentication-passwordless-security-key#fido-security-key-optional-settings>`_ Nitrokey FIDO2 is supported by Azure Entra ID out of the box.

.. _fido2-resident-difference-nonresident:

.. faq:: What is the difference between Non-Resident Keys and Resident?

   A non-resident key (non-discoverable credential) is the default credential type created when the user registers their Nitrokey FIDO2 with an authentication system that supports FIDO2/WebAuthn.
   The authentication system stores the key handle, while the private key remains securely inside the Nitrokey.
   This configuration uses no storage space on the Nitrokey and depends on the authentication system to supply the key handle during login.
   The FIDO2 PIN controls access to the Nitrokey and authorizes all operations involving private keys.

   A resident key (discoverable credential) is stored directly on the Nitrokey, including all credential information and metadata required for authentication.
   This allows the credential to be found automatically by the authentication system without providing an external key handle and enables username-less authentication.
   Resident credentials are protected by the FIDO2 PIN, which authorizes their use and ensures that only the authorized user can access them.
   Each credential typically occupies a few hundred bytes of secure storage.



