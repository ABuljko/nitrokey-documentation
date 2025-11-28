Nitrokey FIDO2 FAQ
==================

.. faq:: Which Operating Systems are supported?

   Windows, Linux, macOS, and Android

.. faq:: What can I use the Nitrokey for?

   See the `overview <https://www.nitrokey.com/products/nitrokeys>`_ of supported use cases.

.. faq:: What happens if I lose my Nitrokey?

   When securing accounts using FIDO (two-factor authentication and
   passwordless login), you should configure another factor in your account as
   a backup. Depending on the service/website this backup factor can be a phone number,
   an app or another Nitrokey. In the last case, if you lose one Nitrokey you
   can still log in with the second Nitrokey (or with another second
   factor).

.. faq:: How large is the storage capacity?

   The Nitrokey 3 and Nitrokey Passkey don't contain storage capability for ordinary file (it can only store cryptographic keys).

.. faq:: How many FIDO credentials can my Nitrokey store?

   It can store an unlimited number of non-discoverable credentials. The `factsheet <https://www.nitrokey.com/files/doc/Nitrokey_3_factsheet.pdf>`_ states the amount of discoverable credentials resp. resident keys.

.. faq:: How to use Nitrokey with Azure Entra ID (Active Directory)?

   Some Nitrokey models are supported by Azure Entra ID out of the box. For some Nitrokey models you need to `disable Enforce Attestation <https://learn.microsoft.com/en-us/azure/active-directory/authentication/howto-authentication-passwordless-security-key#fido-security-key-optional-settings>`_.

.. _fido2-resident-difference-nonresident:

.. faq:: What is the difference between Non-Resident Keys and Resident?

   A non-discoverable credential (also: non-resident key) is the default credential type created when the user registers their Nitrokey with an authentication system that supports FIDO2/WebAuthn.
   This configuration uses no storage space on the Nitrokey and depends on the authentication system to supply the key handle during login.
   Therefore an unlimited amount of credentials can be used with a Nitrokey. During login users have to enter their user name.

   A discoverable credential (also: resident key) is stored directly on the Nitrokey, including all required credential information and metadata.
   This allows the credential to be found automatically by the authentication system without providing an external key handle and enables username-less authentication.
   Each credential typically occupies a few hundred bytes of secure storage, thus limiting the amount of credentials used with a Nitrokey (see
   `factsheet <https://www.nitrokey.com/files/doc/Nitrokey_3_factsheet.pdf>`_).
