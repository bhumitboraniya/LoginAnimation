# LoginAnimationz



# 1. Add the Rive dependency
dependencies {
    implementation 'app.rive:rive-android:5.0.0'
    implementation "androidx.startup:startup-runtime:1.1.1"
}


# 2.  Initializing Rive in AndroidManifest.xml
<provider
  android:name="androidx.startup.InitializationProvider"
  android:authorities="${applicationId}.androidx-startup"
  android:exported="false"
  tools:node="merge">
    <meta-data android:name="app.rive.runtime.kotlin.RiveInitializer"
      android:value="androidx.startup" />
</provider>


# 3.Add RiveAnimation to your layout
<app.rive.runtime.kotlin.RiveAnimationView
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    app:riveResource="@raw/off_road_car_blog" />

