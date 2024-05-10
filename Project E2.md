## 连接手机
![](https://img-blog.csdnimg.cn/img_convert/55c79f0f2c50f0e311a8f3404b9b46ef.png)

## 构建应用
![](https://img-blog.csdnimg.cn/img_convert/bacead412dc57629bca0236b591e6697.png)

## 将应用传输到手机里并安装
![](https://img-blog.csdnimg.cn/img_convert/17336ee11c85a1e56cd130642e70ce44.jpeg)

## 查看安装完的应用
![](https://img-blog.csdnimg.cn/img_convert/28738daf8d222f4d8370b3825826d11e.jpeg)
![](https://img-blog.csdnimg.cn/img_convert/52724e5d5fd56439efee28960d3c5113.jpeg)

## fragment_first.xml 代码
```kotlin
	<?xml version="1.0" encoding="utf-8"?>
	<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
	    xmlns:app="http://schemas.android.com/apk/res-auto"
	    xmlns:tools="http://schemas.android.com/tools"
	    android:background="@color/screenBackground"
	
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    tools:context=".FirstFragment">
	
	    <TextView
	        android:id="@+id/textview_first"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:background="@color/white"
	        android:fontFamily="sans-serif-condensed"
	        android:text="@string/hello_first_fragment"
	
	        android:textColor="@android:color/darker_gray"
	        android:textSize="72sp"
	        android:textStyle="bold"
	        app:layout_constraintBottom_toBottomOf="parent"
	        app:layout_constraintEnd_toEndOf="parent"
	        app:layout_constraintStart_toStartOf="parent"
	        app:layout_constraintTop_toTopOf="parent"
	        app:layout_constraintVertical_bias="0.3" />
	
	    <Button
	
	        android:id="@+id/random_button"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_marginEnd="24dp"
	        android:background="@color/buttonBackground"
	        android:text="@string/random_button_text"
	        app:layout_constraintBottom_toBottomOf="parent"
	        app:layout_constraintEnd_toEndOf="parent"
	        app:layout_constraintTop_toBottomOf="@+id/textview_first"
	        app:layout_constraintVertical_bias="0.501"
	
	
	        />
	
	    <Button
	        android:id="@+id/toast_button"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:layout_marginStart="24dp"
	        android:background="@color/buttonBackground"
	        android:text="@string/toast_button_text"
	        app:layout_constraintBottom_toBottomOf="parent"
	        app:layout_constraintEnd_toStartOf="@+id/random_button"
	        app:layout_constraintHorizontal_bias="0.0"
	        app:layout_constraintStart_toStartOf="parent"
	        app:layout_constraintTop_toBottomOf="@+id/textview_first"
	        app:layout_constraintVertical_bias="0.501" />
	
	    <Button
	        android:id="@+id/count_button"
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:text="@string/count_button_text"
	        android:background="@color/buttonBackground"
	        app:layout_constraintBottom_toBottomOf="parent"
	        app:layout_constraintEnd_toStartOf="@+id/random_button"
	        app:layout_constraintHorizontal_bias="0.55"
	        app:layout_constraintStart_toEndOf="@+id/toast_button"
	        app:layout_constraintTop_toBottomOf="@+id/textview_first"
	        app:layout_constraintVertical_bias="0.501" />
	
	</androidx.constraintlayout.widget.ConstraintLayout>
```
## fragment_second 代码
```kotlin
	<?xml version="1.0" encoding="utf-8"?>
	<androidx.core.widget.NestedScrollView xmlns:android="http://schemas.android.com/apk/res/android"
	    xmlns:app="http://schemas.android.com/apk/res-auto"
	    xmlns:tools="http://schemas.android.com/tools"
	    android:layout_width="match_parent"
	    android:background="@color/screenBackground2"
	    android:layout_height="match_parent"
	    tools:context=".SecondFragment">
	
	    <androidx.constraintlayout.widget.ConstraintLayout
	        android:layout_width="wrap_content"
	        android:layout_height="wrap_content"
	        android:padding="16dp">
	
	
	        <Button
	            android:id="@+id/button_second"
	            android:layout_width="wrap_content"
	            android:layout_height="wrap_content"
	            android:text="@string/previous"
	            app:layout_constraintBottom_toBottomOf="parent"
	            app:layout_constraintEnd_toEndOf="parent"
	            app:layout_constraintHorizontal_bias="0.498"
	            app:layout_constraintStart_toStartOf="parent"
	            app:layout_constraintTop_toTopOf="parent"
	            app:layout_constraintVertical_bias="1.0" />
	
	        <TextView
	            android:id="@+id/textview_header"
	            android:layout_width="wrap_content"
	            android:layout_height="wrap_content"
	            android:layout_marginStart="24dp"
	            android:layout_marginTop="64dp"
	            android:layout_marginEnd="24dp"
	            android:text="@string/random_heading"
	            android:textColor="@color/colorPrimaryDark"
	            android:textSize="24sp"
	            app:layout_constraintEnd_toEndOf="parent"
	            app:layout_constraintStart_toStartOf="parent"
	            app:layout_constraintTop_toTopOf="parent" />
	
	        <TextView
	            android:id="@+id/textview_random"
	            android:layout_width="wrap_content"
	            android:layout_height="wrap_content"
	            android:text="@string/R"
	            android:textColor="@android:color/white"
	            android:textSize="72sp"
	            android:textStyle="bold"
	            app:layout_constraintBottom_toTopOf="@+id/button_second"
	            app:layout_constraintEnd_toEndOf="parent"
	            app:layout_constraintHorizontal_bias="0.498"
	            app:layout_constraintStart_toStartOf="parent"
	            app:layout_constraintTop_toBottomOf="@+id/textview_header"
	            app:layout_constraintVertical_bias="1.0" />
	
	
	    </androidx.constraintlayout.widget.ConstraintLayout>
	</androidx.core.widget.NestedScrollView>
```
## 颜色文件 colors.xml 代码
```kotlin
	<?xml version="1.0" encoding="utf-8"?>
	<resources>
	    <color name="black">#FF000000</color>
	    <color name="white">#FFFFFFFF</color>
	    <color name="screenBackground">#2196F3</color>
	    <color name="buttonBackground">#BBDEFB</color>
	    <color name="colorPrimaryDark">#3700B3</color>
	    <color name="screenBackground2">#26C6DA</color>
	</resources>
```
## 字体文件 strings.xml 代码
```kotlin
    <string name="toast_button_text">Toast</string>
    <string name="random_button_text">Random</string>
    <string name="count_button_text">Count</string>
    <string name="count_text">0</string>
    <string name="hello_first_fragment">0</string>
    <string name="random_heading">Here is a random number between 0 and %d.</string>
    <string name="R">R</string>
 ```

# nav_graph.xml 代码
```kotlin
	<?xml version="1.0" encoding="utf-8"?>
	<navigation xmlns:android="http://schemas.android.com/apk/res/android"
	    xmlns:app="http://schemas.android.com/apk/res-auto"
	    xmlns:tools="http://schemas.android.com/tools"
	    android:id="@+id/nav_graph"
	    app:startDestination="@id/FirstFragment">
	
	    <fragment
	        android:id="@+id/FirstFragment"
	        android:name="com.example.myapplication.FirstFragment"
	        android:label="@string/first_fragment_label"
	        tools:layout="@layout/fragment_first">
	
	        <action
	            android:id="@+id/action_FirstFragment_to_SecondFragment"
	            app:destination="@id/SecondFragment"
	            app:popUpTo="@id/nav_graph"
	            app:popUpToInclusive="true"/>
	    </fragment>
	    <fragment
	        android:id="@+id/SecondFragment"
	        android:name="com.example.myapplication.SecondFragment"
	        android:label="@string/second_fragment_label"
	        tools:layout="@layout/fragment_second">
	
	        <action
	            android:id="@+id/action_SecondFragment_to_FirstFragment"
	            app:destination="@id/FirstFragment" />
	        <argument
	            android:name="myArg"
	            app:argType="integer" />
	    </fragment>
	</navigation>
```
## 安装SafeArg
### 1.  build.gradle.kts(Project) 的代码
```kotlin
	// Top-level build file where you can add configuration options common to all sub-projects/modules.
	plugins {
	    alias(libs.plugins.androidApplication) apply false
	    alias(libs.plugins.jetbrainsKotlinAndroid) apply false
	
	}
	buildscript {
	    repositories {
	        google()
	    }
	    dependencies {
	        val nav_version = "2.7.7"
	        classpath("androidx.navigation:navigation-safe-args-gradle-plugin:$nav_version")
	    }
	}
```
### 2. build.gradle.kts(Module) 的代码
```kotlin
	plugins {
	    alias(libs.plugins.androidApplication)
	    alias(libs.plugins.jetbrainsKotlinAndroid)
	    id("androidx.navigation.safeargs.kotlin")
	}
	
	android {
	    namespace = "com.example.myapplication"
	    compileSdk = 34
	
	    defaultConfig {
	        applicationId = "com.example.myapplication"
	        minSdk = 24
	        targetSdk = 34
	        versionCode = 1
	        versionName = "1.0"
	
	        testInstrumentationRunner = "androidx.test.runner.AndroidJUnitRunner"
	    }
	
	    buildTypes {
	        release {
	            isMinifyEnabled = false
	            proguardFiles(getDefaultProguardFile("proguard-android-optimize.txt"), "proguard-rules.pro")
	        }
	    }
	    compileOptions {
	        sourceCompatibility = JavaVersion.VERSION_1_8
	        targetCompatibility = JavaVersion.VERSION_1_8
	    }
	    kotlinOptions {
	        jvmTarget = "1.8"
	    }
	    buildFeatures {
	        viewBinding = true
	    }
	}
	
	dependencies {
	
	    implementation(libs.androidx.core.ktx)
	    implementation(libs.androidx.appcompat)
	    implementation(libs.material)
	    implementation(libs.androidx.constraintlayout)
	    implementation(libs.androidx.navigation.fragment.ktx)
	    implementation(libs.androidx.navigation.ui.ktx)
	    testImplementation(libs.junit)
	    androidTestImplementation(libs.androidx.junit)
	    androidTestImplementation(libs.androidx.espresso.core)
	}

```
## 在build.gradle.kts中添加SafeArg后点击"sync"即可自动安装依赖
## 在FristFragment.kt中添加onViewCreated()方法用于3个按钮的功能

```kotlin
override fun onViewCreated(view: View, savedInstanceState: Bundle?) {
    super.onViewCreated(view, savedInstanceState)


    binding.countButton.setOnClickListener {
        findNavController().navigate(R.id.action_FirstFragment_to_SecondFragment)
    }
    // find the toast_button by its ID and set a click listener
    view.findViewById<Button>(R.id.toast_button).setOnClickListener {
        // create a Toast with some text, to appear for a short time
        val myToast = Toast.makeText(context, "Hello Toast!", Toast.LENGTH_LONG)
        // show the Toast
        myToast.show()
    }

    view.findViewById<Button>(R.id.count_button).setOnClickListener {
        countMe(view)
    }
    view.findViewById<Button>(R.id.random_button).setOnClickListener {
        val showCountTextView = view.findViewById<TextView>(R.id.textview_first)
        val currentCount = showCountTextView.text.toString().toInt()
        val action = FirstFragmentDirections.actionFirstFragmentToSecondFragment(currentCount)
        findNavController().navigate(action)

    }
}
```

## 添加countMe()方法用于计数

```kotlin
private fun countMe(view: View) {
    // Get the text view
    val showCountTextView = view.findViewById<TextView>(R.id.textview_first)

    // Get the value of the text view.
    val countString = showCountTextView.text.toString()

    // Convert value to a number and increment it
    var count = countString.toInt()
    count++

    // Display the new value in the text view.
    showCountTextView.text = count.toString()
}
```
## 在SecondFragment.kt中导入navArgs
```kotlin
import androidx.navigation.fragment.navArgs
```

## 在SecondFragment.kt中添加显示随机数的代码
```kotlin
val args: SecondFragmentArgs by navArgs()
    override fun onViewCreated  (view: View, savedInstanceState: Bundle?) {

        super.onViewCreated(view, savedInstanceState)

        binding.buttonSecond.setOnClickListener {
            findNavController().navigate(R.id.action_SecondFragment_to_FirstFragment)
        }
        val count = args.myArg
        val countText = getString(R.string.random_heading, count)
        view.findViewById<TextView>(R.id.textview_header).text = countText
        val random = java.util.Random()
        var randomNumber = 0
        if (count > 0) {
            randomNumber = random.nextInt(count + 1)
        }
        view.findViewById<TextView>(R.id.textview_random).text = randomNumber.toString()

    }
```

## 在SecondFragment的Arguments中添加myArg
![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/c14e4a8669224269ae7b7805fd0503e1.png)

# 运行应用程序，查看运行结果
## 应用主界面
![](https://img-blog.csdnimg.cn/img_convert/2e45f56e6eba825b70e794b034506195.jpeg)

## Toast功能演示
![](https://img-blog.csdnimg.cn/img_convert/34e2aee0e284428cb4baedb453d44bcc.jpeg)

## Random功能演示
![](https://img-blog.csdnimg.cn/img_convert/45b89537230349bac2731d55f63d6e37.jpeg)

## 第二页Random功能演示
![](https://img-blog.csdnimg.cn/img_convert/1c58d4a716a6e42070aea1fb0fc98080.jpeg)

