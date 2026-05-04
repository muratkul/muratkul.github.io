# Momentum — Privacy Policy

**Effective date:** 2026-05-04  
**Last updated:** 2026-05-04  
**Data controller:** Murat Kul (independent developer)  
**Contact:** nfvwzhbrbw@privaterelay.appleid.com

Momentum (the "App") is a personal finance tracking mobile application.
This Privacy Policy explains what data we collect when you use Momentum,
how we use it, and what rights you have.

---

## 1. Data We Collect

We only collect data that's necessary to run the app.

### 1.1. Account data
- **Email address** — for sign-up and login
- **Password** — stored as a hash by Firebase Authentication. We never
  see your plaintext password and don't store it on our servers.

### 1.2. Financial data (app content)
You enter this data yourself; we don't pull it from anywhere:
- Assets (name, category, amount, currency, description)
- Liabilities (name, category, amount, currency, due date, interest rate)
- Monthly snapshots (point-in-time photos of your asset/liability values)
- Expenses (name, category, amount, date)
- Preferences (base currency, language, theme, snapshot day)

### 1.3. Device data
- The local cache (Hive) only stores **exchange rates**. Personal data
  is **not persisted** on the device — all user data lives in Google
  Cloud Firestore.

### 1.4. Data we don't collect
- ❌ Advertising identifiers (IDFA / GAID)
- ❌ Location data
- ❌ Contacts, photos, or file system access
- ❌ Usage analytics or behavior tracking (no third-party analytics SDK)
- ❌ Bank API integration (manual data entry only)

---

## 2. How We Use Your Data

| Purpose | Data |
|---|---|
| Sign you in to your account | Email, password (hash) |
| Store and sync your data across devices | All financial data |
| Normalize amounts across multiple currencies | Exchange rates (cached locally) |
| Respond to lawful requests from authorities | Account identifier |

We **do not** use your data for advertising, profiling, sale, or
marketing. We don't sell or share your data with third parties.

---

## 3. Where Your Data Is Stored

- **Google Cloud Firestore** (Google LLC, US/EU servers). Firebase
  Security Rules ensure that only the signed-in user can access their
  own data; other users cannot.
- **Your device** (local Hive cache — only exchange rates).

Firebase's own privacy policy:
https://firebase.google.com/support/privacy

---

## 4. Third-Party Services

| Service | Purpose | Data sent |
|---|---|---|
| Firebase Authentication (Google) | User authentication | Email, password hash |
| Cloud Firestore (Google) | Data storage and sync | Financial data, preferences |
| OpenExchangeRates API | Live exchange rates | Anonymous API request only — no user data sent |

Apple's own policies apply during App Store download/install.

---

## 5. Data Retention

- Your data is retained as long as your account is active.
- When you delete your account (Settings → Delete Account), all your
  financial data is removed from Firestore, then your credentials are
  removed from Firebase Authentication. **This action cannot be undone.**
- A 30-day technical lag may exist in backups (Google Firebase's
  infrastructure backup policy).

---

## 6. Your Rights (GDPR / KVKK)

As a data subject, you have these rights:

- ✅ **Access**: You can see what data we hold — all of it is visible
  inside the app.
- ✅ **Rectification**: You can edit incorrect data inside the app.
- ✅ **Erasure (right to be forgotten)**: Settings → Delete Account
  removes all your data with one tap.
- ✅ **Portability**: Settings → Export Data lets you export your data
  as CSV or PDF.
- ✅ **Object to processing**: Email us — we'll respond within 30 days.

For GDPR / KVKK requests, contact us via email above.

---

## 7. Children's Privacy

Momentum is not directed at users under 13. If we discover that an
under-13 user has registered, we'll delete the account.

---

## 8. Security

- All data in transit is encrypted with TLS (HTTPS).
- Firestore Security Rules restrict each user to their own data
  (`request.auth.uid == userId`).
- Your password is never stored in plaintext; Firebase Auth hashes it
  with PBKDF2-SHA256.
- The local device cache (Hive) does not contain financial data.

No system is 100% secure. If we discover a security breach, we'll
notify you within 72 hours as required by law.

---

## 9. Changes to This Policy

If this policy is updated, we'll update the effective date at the top.
For material changes, we'll also show an in-app notice.

---

## 10. Contact

For data requests, questions, or concerns:  
**Email:** nfvwzhbrbw@privaterelay.appleid.com

---

**⚠️ Note:** This text is a draft. Before publishing, please have a
legal professional review it (especially for GDPR and KVKK compliance).
