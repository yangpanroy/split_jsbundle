### split js bundle

react-native bundle --platform ios --dev false --entry-file base.js --bundle-output build/ios/common.jsbundle --assets-dest build/ios/

react-native bundle --platform ios --dev false --entry-file index.js --bundle-output build/ios/main_app_all.jsbundle --assets-dest build/ios/

react-native bundle --platform ios --dev false --entry-file rewards/index.js --bundle-output build/ios/sub_app_all.jsbundle --assets-dest build/ios/

node diff.js ./build/ios/common.jsbundle ./build/ios/main_app_all.jsbundle ./build/ios/main_app.jsbundle
node diff.js ./build/ios/common.jsbundle ./build/ios/sub_app_all.jsbundle ./build/ios/sub_app.jsbundle

