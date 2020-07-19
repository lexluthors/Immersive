# Immersive
[![](https://img.shields.io/badge/platform-android-orange.svg)](https://github.com/hacknife) [![](https://img.shields.io/badge/language-java-yellow.svg)](https://github.com/hacknife) [![](https://img.shields.io/badge/Jcenter-1.1.0-brightgreen.svg)](https://github.com/hacknife) [![](https://img.shields.io/badge/build-passing-brightgreen.svg)](https://github.com/hacknife) [![](https://img.shields.io/badge/license-apache--2.0-green.svg)](https://github.com/hacknife) [![](https://img.shields.io/badge/api-19+-green.svg)](https://github.com/hacknife)<br/><br/>
一行代码实现沉浸式，适配android4.4到8.0+，沉浸式前所未有的简单，androidx版本。
</br></br>
![Image Text](https://github.com/hacknife/immersive/blob/master/immersive.gif)
## 代码示例
```Java
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        Immersive.setContentView(this, R.layout.activity_main, R.color.blue, R.color.green, false, false);
    }
}

```
使用以下方法代替Activity.setContentView()，即可实现沉浸式。
```Java
    /**
     * @param activity 当前需要使用沉浸式的Activity
     * @param layoutRes 当前activity使用的布局资源Id
     * @param statusRes 状态栏颜色资源Id
     * @param navigationRes 底部导航栏颜色Id
     * @param statusEmbed 是否隐藏状态栏
     * @param navigationEmbed 是否隐藏导航栏
     */
    Immersive.setContentView(Activity activity, @LayoutRes int layoutRes, int statusRes, int navigationRes, boolean statusEmbed, boolean navigationEmbed)
```
动态修改状态栏颜色，前提是必须使用Immersive.setContentView设置布局。
```Java
    /**
     *
     * @param activity 当前Activity
     * @param color 颜色
     */
    Immersive.setStatusBarColor(Activity activity, int color)
```
动态修改导航栏颜色，前提是必须使用Immersive.setContentView设置布局。
```Java
    /**
     *
     * @param activity 当前Activity
     * @param color 颜色
     */
    Immersive.setNavigationBarColor(Activity activity, int color)
```
 
#### 快速引入项目
```Java
	dependencies {
                ...
	        implementation 'com.apecoder:immersive:0.0.1'
	}
```

<br><br><br>
## 感谢
https://github.com/hacknife/immersive
