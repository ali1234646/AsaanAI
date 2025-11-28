
git remote add origin https://github.com/YOUR_USERNAME/AsaanAI-starter.git
git branch -M main
git push -u origin maincd backend
# npm init پہلے ہو چکا ہوگا اگر package.json add کیا
npm install
# .env بنائیں، .env.example کو دیکھ کر اپنی keys ڈال دیں
cp .env.example .env
# پھر .env میں OPENAI_KEY اور FIREBASE keys ڈالیں (vim/nano/VSCode)
node index.js
# یا dev میں:
npm run devFIREBASE_PROJECT_ID=project-id
FIREBASE_CLIENT_EMAIL=...@...gserviceaccount.com
FIREBASE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\nMIIE... \n-----END PRIVATE KEY-----\n"
OPENAI_KEY=sk-...
PORT=3000rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
