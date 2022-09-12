---
title: क्लाइंट-सर्वर आर्किटेक्चर (Client-Server Architecture)
status: Completed
category: अवधारणा
---

## यह क्या है 

क्लाइंट-सर्वर आर्किटेक्चर में, एप्लिकेशन बनाने वाला लॉजिक (या कोड) दो या दो से अधिक कंपोनेंट्स के बीच विभाजित होता है: एक क्लाइंट, जो काम करने के लिए कहता है (उदाहरण के लिए आपके वेब ब्राउज़र में चल रहा Gmail वेब एप्लिकेशन), और एक या अधिक सर्वर जो उस रिक्वेस्ट को पूरा करते हैं (उदाहरण के लिए, क्लाउड में Google के कंप्यूटर पर चलने वाली "ईमेल भेजें" सर्विस)। यह पुराने ऍप्लिकेशन्स के साथ विरोधाभासी है जो आम तौर पर स्व-निहित थे (जैसे कि 1990 के दशक में डेस्कटॉप ऍप्लिकेशन्स) और एक ही स्थान पर सभी काम करते थे (उदाहरण में, email आपके अपने कंप्यूटर के बजाय Google के कंप्यूटर द्वारा भेजा जाता है)।

## समस्या  

क्लाइंट-सर्वर आर्किटेक्चर एक बड़ी चुनौती को हल करता है जिसमें स्वयं निहित ऍप्लिकेशन्स होते हैं: नियमित अपडेट। एक स्व-निहित ऐप में, प्रत्येक अपडेट के लिए, उपयोगकर्ताओं को नवीनतम संस्करण को डाउनलोड और इंस्टॉल करना होगा। कल्पना कीजिए कि Amazon के सभी उत्पाद कैटलॉग को ब्राउज़ करने में सक्षम होने से पहले अपने कंप्यूटर पर डाउनलोड करना पड़े!

## समाधान 

रिमोट सर्वर या सर्विस में एप्लिकेशन लॉजिक को लागू करके, ऑपरेटर क्लाइंट-साइड पर लॉजिक को बदलने की आवश्यकता के बिना ही, इसे अपडेट कर सकते हैं। इसका मतलब है कि अपडेट अधिक बार किए जा सकते हैं। सर्वर पर डेटा स्टोर करने से कई क्लाइंट एक ही डेटा को देख और साझा कर सकते हैं। पारंपरिक तौर पर, ऑफ़लाइन वर्ड प्रोसेसर की तुलना में ऑनलाइन वर्ड प्रोसेसर का उपयोग करने के बीच अंतर पर विचार करें। ऑफ़लाइन में, आपकी फ़ाइलें सर्वर-साइड पर मौजूद होती हैं और अन्य उपयोगकर्ताओं के साथ साझा की जा सकती हैं जो उन्हें सर्वर से आसानी से डाउनलोड करते हैं। पहले, फ़ाइलों को हटाने योग्य मीडिया (फ्लॉपी डिस्क!)में कॉपी करके, उपयोगकर्ताओं के साथ साझा करने की आवश्यकता होती थी। 