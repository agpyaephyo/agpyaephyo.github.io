## MMTextView
An android library that display correct Myanmar text in both unicode & zawgyi phones.
All the App Data has to be in **_UNICODE_** to use this library.

### Step-1: Update your {root}/build.gradle
```groovy
allprojects {
    repositories {
        jcenter()
        maven { url 'https://dl.bintray.com/agpyaephyo/android' }
    }
}
```

### Step-2: Update your {app}/build.gradle
```
implementation 'org.mmtextview:mmtextview:1.4'
```

### Eg-1: Simple UI Components
```xml
<org.mmtextview.components.MMTextView
    android:id="@+id/lbl"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_centerInParent="true"
    android:text="@string/click_me" />

<org.mmtextview.components.MMButton
    android:id="@+id/btn_show_loading"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="@string/show_loading" />
```
![Eg-1](https://user-images.githubusercontent.com/2491168/36755341-45c24180-1c3a-11e8-9899-dffc2a71fc58.png)

You can use **MMCheckBox** and **MMRadioButton** in this way as well.

### Eg-2: NavigationView
```xml
<org.mmtextview.components.complex.MMNavigationView
    android:id="@+id/navigation_view"
    android:layout_width="270dp"
    android:layout_height="match_parent"
    android:layout_gravity="start"
    app:headerLayout="@layout/view_pod_login_user"
    app:itemTextColor="@color/primary_text"
    app:menu="@menu/left_menu_news" />
```
![Eg-2](https://user-images.githubusercontent.com/2491168/36755572-ffb4bdfc-1c3a-11e8-92bd-a1343de74818.png)

### Eg-3: TabLayout
```xml
<org.mmtextview.components.complex.MMTabLayout
    android:id="@+id/tl_news_by_category"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    app:tabIndicatorColor="@color/colorAccent"
    app:tabSelectedTextColor="@color/white_full"
    app:tabTextColor="@color/grey"
    android:visibility="gone"
    />
```
![Eg-3](https://user-images.githubusercontent.com/2491168/36755642-34524fa2-1c3b-11e8-800a-743b3ee7bf4a.png)

### Eg-4: ProgressDialog
```java
MMProgressDialog progressDialog = new MMProgressDialog(getContext());
progressDialog.setMessage("ဘာတွေ ဖြစ်ကုန်ပြီလဲ အရပ်ကတို့");
progressDialog.show();
```
![Eg-4](https://user-images.githubusercontent.com/2491168/36756082-73887150-1c3c-11e8-9d5f-79ba8b12093b.gif)

### Eg-5 : Snackbar (with Helper Method)
```java
mSnackbar = Snackbar.make(toolbar, "ဘာလို့ လျောက်နှိပ်ရတာတုန်း", Snackbar.LENGTH_INDEFINITE)
                .setAction("တော်ပြီ", new View.OnClickListener() {
                    @Override
                    public void onClick(View v) {
                        mSnackbar.dismiss();
                    }
                });
MMFontUtils.applyMMFontToSnackBar(mSnackbar);
```
![Eg-5](https://user-images.githubusercontent.com/2491168/36755839-ca1759ba-1c3b-11e8-9da2-c115f965565f.png)
