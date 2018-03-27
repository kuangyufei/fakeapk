# fakeapk

功能强大的android hook 工具，全部开源，配合 xposed 神器使用  

### QQ群 720098517  微信：15817321796  验证注明：fakeapk 

可配合盘古后台系统,  lua脚本 等工具使用。

|工具名称| 下载链接|备注|
|----|-----|---|
|盘古后台系统|https://gitee.com/kuangyufei/pangu|盘古系统后台|
|lua|https://gitee.com/kuangyufei/luaforad|可刷多种广告SDK 脚本工具|
|盘古VPN系统|https://gitee.com/kuangyufei/pangu_vpn|vpn自动选择，切换工具|
|盘古管理系统|https://gitee.com/kuangyufei/pangu_manage|实时查看各广告平台刷量数据，包括留存比例，水军量，转化率等等|

```

/**
 * Created by turingkuang on 2017/1/9.
 */
public class SystemPropertiesHook extends XC_MethodHook {
    public SystemPropertiesHook() {
        super();
    }

    protected void beforeHookedMethod(MethodHookParam param) throws Throwable {
        String methodName = param.method.getName();
        if (methodName.startsWith("get")) {
            if (!TextUtils.isEmpty(SharedPref.getXValue("Build.HARDWARE"))) {
                KernelLogUtil.LogXposed("SystemPropertiesHook -Build.HARDWARE- " + SharedPref.getXValue("Build.HARDWARE"));
                XposedHelpers.setStaticObjectField(android.os.Build.class, "HARDWARE", SharedPref.getXValue("Build.HARDWARE"));
            }

            if (!TextUtils.isEmpty(SharedPref.getXValue("Build.PRODUCT"))) {
                KernelLogUtil.LogXposed("SystemPropertiesHook -Build.PRODUCT- " + SharedPref.getXValue("Build.PRODUCT"));
                XposedHelpers.setStaticObjectField(android.os.Build.class, "PRODUCT", SharedPref.getXValue("Build.PRODUCT"));
            }

            if (!TextUtils.isEmpty(SharedPref.getXValue("Build.DEVICE"))) {
                KernelLogUtil.LogXposed("SystemPropertiesHook -Build.DEVICE- " + SharedPref.getXValue("Build.DEVICE"));
                XposedHelpers.setStaticObjectField(android.os.Build.class, "DEVICE", SharedPref.getXValue("Build.DEVICE"));
            }

            if (!TextUtils.isEmpty(SharedPref.getXValue("Build.CPU_ABI"))) {
                KernelLogUtil.LogXposed("SystemPropertiesHook -Build.CPU_ABI- " + SharedPref.getXValue("Build.CPU_ABI"));
                XposedHelpers.setStaticObjectField(android.os.Build.class, "CPU_ABI", SharedPref.getXValue("Build.CPU_ABI"));
            }


            if (!TextUtils.isEmpty(SharedPref.getXValue("Build.MODEL"))) {
                KernelLogUtil.LogXposed("SystemPropertiesHook -Build.MODEL- " + SharedPref.getXValue("Build.MODEL"));
                XposedHelpers.setStaticObjectField(android.os.Build.class, "MODEL", SharedPref.getXValue("Build.MODEL"));
            }

            if (!TextUtils.isEmpty(SharedPref.getXValue("Build.MANUFACTURER"))) {
                KernelLogUtil.LogXposed("SystemPropertiesHook -Build.MANUFACTURER- " + SharedPref.getXValue("Build.MANUFACTURER"));
                XposedHelpers.setStaticObjectField(android.os.Build.class, "MANUFACTURER", SharedPref.getXValue("Build.MANUFACTURER"));
            }

            if (!TextUtils.isEmpty(SharedPref.getXValue("Build.BOARD"))) {
                KernelLogUtil.LogXposed("SystemPropertiesHook -Build.BOARD- " + SharedPref.getXValue("Build.BOARD"));
                XposedHelpers.setStaticObjectField(android.os.Build.class, "BOARD", SharedPref.getXValue("Build.BOARD"));
            }

            if (!TextUtils.isEmpty(SharedPref.getXValue("Build.BRAND"))) {
                KernelLogUtil.LogXposed("SystemPropertiesHook -Build.BRAND- " + SharedPref.getXValue("Build.BRAND"));
                XposedHelpers.setStaticObjectField(android.os.Build.class, "BRAND", SharedPref.getXValue("Build.BRAND"));
            }

            if (!TextUtils.isEmpty(SharedPref.getXValue("Build.DISPLAY"))) {
                KernelLogUtil.LogXposed("SystemPropertiesHook -Build.DISPLAY- " + SharedPref.getXValue("Build.DISPLAY"));
                XposedHelpers.setStaticObjectField(android.os.Build.class, "DISPLAY", SharedPref.getXValue("Build.DISPLAY"));
            }

            if (!TextUtils.isEmpty(SharedPref.getXValue("Build.HOST"))) {
                KernelLogUtil.LogXposed("SystemPropertiesHook -Build.HOST- " + SharedPref.getXValue("Build.HOST"));
                XposedHelpers.setStaticObjectField(android.os.Build.class, "HOST", SharedPref.getXValue("Build.HOST"));
            }

            if (!TextUtils.isEmpty(SharedPref.getXValue("Build.FINGERPRINT"))) {
                KernelLogUtil.LogXposed("SystemPropertiesHook -Build.FINGERPRINT- " + SharedPref.getXValue("Build.FINGERPRINT"));
                XposedHelpers.setStaticObjectField(android.os.Build.class, "FINGERPRINT", SharedPref.getXValue("Build.FINGERPRINT"));
				
```