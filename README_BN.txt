ROY CYBER CAFE Billing — Android APK Build Project

এই প্রকল্পটি Android অ্যাপের APK তৈরি করার জন্য। বর্তমান ওয়েবসাইটের ফাইল/পেমেন্ট সিস্টেম এতে বদলানো হয়নি। বিলিং HTML অ্যাপের ভিতরে অফলাইনে রাখা হয়েছে।

APK তৈরি করতে GitHub Actions ব্যবহার:
1. GitHub অ্যাকাউন্ট তৈরি/লগইন করুন: https://github.com
2. নতুন Public বা Private repository তৈরি করুন, নাম দিন roy-cyber-cafe-billing (README যোগ করা ঐচ্ছিক)।
3. ZIP ফাইল Extract করে সব ফাইল ও ফোল্ডার repository-র মূল জায়গায় আপলোড করুন। বিশেষ করে .github/workflows/build-apk.yml ফাইলের পথ একই থাকতে হবে।
4. Commit changes করুন। Repository-তে Actions ট্যাব খুলুন। “Build ROY CYBER CAFE APK” workflow নির্বাচন করে “Run workflow” চাপুন (অথবা push-এর পর workflow নিজে শুরু হবে)।
5. কাজ সফল হলে workflow run-এর নিচে Artifacts থেকে “ROY-CYBER-CAFE-APK” ডাউনলোড করুন। ZIP খুললে app-debug.apk পাবেন। সেটিই APK; artifact ZIP-কে সরাসরি ইনস্টল করবেন না।
6. APK ফোনে খুলে Install করুন। Android জিজ্ঞেস করলে এই উৎস থেকে install করার অনুমতি দিন।

গুরুত্বপূর্ণ:
- এই build প্রকল্প থেকে এখনো APK compile করা হয়নি; GitHub Actions-এ build সফল হওয়ার পরই APK তৈরি হবে।
- প্রথমে পরীক্ষামূলক বিল, cash payment এবং payment-confirmation lock পরীক্ষা করুন।
- WebView localStorage ডেটা একই অ্যাপ ইনস্টলেশনের মধ্যে থাকে। অ্যাপের ডেটা মুছলে বা অ্যাপ uninstall করলে ডেটা হারাতে পারে; নিয়মিত backup রাখুন।
