# घरचा किराणा – Family Sync V4

## फोनवरून सेटअप
1. Firebase Console > Firestore Database > Rules मध्ये `firestore.rules` मधील संपूर्ण मजकूर Paste करा आणि **Publish** करा. Rules publish होईपर्यंत डेटाबेस बंद ठेवा.
2. GitHub repository मध्ये `index.html` फाइल root मध्ये Upload करा (Add file > Upload files).
3. GitHub Settings > Pages > Build and deployment > Deploy from a branch > main / (root) > Save. Pages साइट HTTPS वर उघडेल. Private repo वर GitHub Pages उपलब्धता plan नुसार बदलू शकते; उपलब्ध नसेल तर Firebase Hosting वापरा.
4. Firebase Console > Authentication > Settings > Authorized domains मध्ये GitHub Pages चे host नाव (उदा. `username.github.io`) जोडा. Domain verification किंवा provider settings मागितल्यास पूर्ण करा.
5. तिन्ही सदस्यांनी hosted HTTPS URL उघडून Google Login करावा. पहिल्या सदस्याने Create Family करावे आणि 12-character code इतर दोघांना द्यावा. इतर दोघांनी Join Family करावे.
6. एकाच Family मध्ये 3 सदस्यांपर्यंत जोडता येतील. प्रत्येकाने आपला WhatsApp नंबर स्वतःच्या मोबाईलवर भरावा. Final List बटण WhatsApp message draft उघडेल; Send manually करावा लागेल.

## लक्षात ठेवा
- फाइल `file://` किंवा `content://` म्हणून उघडल्यास Google Login / cloud sync चालणार नाही. Hosted HTTPS आवश्यक.
- Web Firebase apiKey हा सार्वजनिक client configuration आहे; service-account private key कधीही upload करू नका.
- एकाच वेळी अनेकांनी संपूर्ण यादी बदलल्यास last-write-wins होऊ शकते; हे production-grade conflict resolution नाही.
- या ZIP मध्ये APK नाही. Cloud sync प्रत्यक्ष Firebase वर तपासलेला नाही.
- 12-अक्षरी family code गुप्त ठेवा; code माहित असलेला Google वापरकर्ता family join करू शकतो. Production मध्ये owner approval आणि App Check जोडणे अधिक सुरक्षित आहे.
