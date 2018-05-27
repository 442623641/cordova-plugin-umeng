# cordova-plugin-umeng

友盟分析

．

#安装
```
cordova plugin add https://github.com/442623641/cordova-plugin-umeng.git --variable APPKEY=${ANDROID_APPKEY}

```
#IOS
```
    #import "UMMobClick/MobClick.h"
    UMConfigInstance.appKey = @"IOS_KEY";  
    UMConfigInstance.channelId = @"App Store"; 
    [MobClick startWithConfigure:UMConfigInstance];  
```

#ANDROID
```	
	/**
     * onCreate中调用
     */
   +initUmengSDK();

    private void initUmengSDK() {
        MobclickAgent.setScenarioType(this, MobclickAgent.EScenarioType.E_UM_NORMAL);
        MobclickAgent.setDebugMode(false);
        MobclickAgent.openActivityDurationTrack(false);
        Log.d("UMPlugin", "UMPlugin SDK inited");
    }
    @Override
    protected void onResume() {
        super.onResume();
        MobclickAgent.onResume(this);
    }

    @Override
    protected void onPause() {
        super.onPause();
        MobclickAgent.onPause(this);
    } 
```
