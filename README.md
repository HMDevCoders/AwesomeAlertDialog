# AwesomeAlertDialog

Custom AlertView Dialogue is the world's most advanced alert view library. Custom AlertView Dialogue includes simple message popups, confirmation alerts, selector popups, action sheet bottom menus, and input/feedback contact forms. 

[![platform](https://img.shields.io/badge/platform-Android-yellow.svg)](https://www.android.com)
[![API](https://img.shields.io/badge/API-11%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=11)
[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0.html)
[![Developed By](https://img.shields.io/badge/Developed%20By-@Hannan_Max-green.svg?style=flat)](https://www.instagram.com/hannan_max/)
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-Awesome%20Alert%20Dialog-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/1065)

## ScreenShot
![image](https://github.com/HMDevCoders/AwesomeAlertDialog/blob/master/screenshot.gif)

## Setup
The simplest way to use AwesomeAlertDialog is to add the library as aar dependency to your build.

**Maven**

	<dependency>
		<groupId>com.github.HMDevCoders</groupId>
		<artifactId>AwesomeAlertDialog</artifactId>
		<version>Tag</version>
		<type>aar</type>
	</dependency>

## Gradle
**Add it in your root build.gradle at the end of repositories:**

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}

**Step 2. Add the dependency**
    
    	dependencies {
		implementation 'com.github.HMDevCoders:AwesomeAlertDialog:1.0'
	}

## Usage

show material progress

    AwesomeAlertDialog pDialog = new AwesomeAlertDialog(this, AwesomeAlertDialog.PROGRESS_TYPE);
    pDialog.getProgressHelper().setBarColor(Color.parseColor("#A5DC86"));
    pDialog.setTitleText("Loading");
    pDialog.setCancelable(false);
    pDialog.show();

![image](https://github.com/pedant/sweet-alert-dialog/raw/master/play_progress.gif)

You can customize progress bar dynamically with materialish-progress methods via **AwesomeAlertDialog.getProgressHelper()**:
- resetCount()
- isSpinning()
- spin()
- stopSpinning()
- getProgress()
- setProgress(float progress)
- setInstantProgress(float progress)
- getCircleRadius()
- setCircleRadius(int circleRadius)
- getBarWidth()
- setBarWidth(int barWidth)
- getBarColor()
- setBarColor(int barColor)
- getRimWidth()
- setRimWidth(int rimWidth)
- getRimColor()
- setRimColor(int rimColor)
- getSpinSpeed()
- setSpinSpeed(float spinSpeed)

thanks to the project [@Hannan Max](https://www.instagram.com/hannan_max) and [@Nilen.patel](https://www.instagram.com/nilen.patel) participation.

more usages about progress, please see the sample.

A basic message???

    new AwesomeAlertDialog(this)
        .setTitleText("Here's a message!")
        .show();

A title with a text under???

    new AwesomeAlertDialog(this)
        .setTitleText("Here's a message!")
        .setContentText("It's pretty, isn't it?")
        .show();

A error message???

    new AwesomeAlertDialog(this, AwesomeAlertDialog.ERROR_TYPE)
        .setTitleText("Oops...")
        .setContentText("Something went wrong!")
        .show();

A warning message???

    new AwesomeAlertDialog(this, AwesomeAlertDialog.WARNING_TYPE)
        .setTitleText("Are you sure?")
        .setContentText("Won't be able to recover this file!")
        .setConfirmText("Yes,delete it!")
        .show();

A success message???

    new AwesomeAlertDialog(this, AwesomeAlertDialog.SUCCESS_TYPE)
        .setTitleText("Good job!")
        .setContentText("You clicked the button!")
        .show();

A message with a custom icon???

    new AwesomeAlertDialog(this, AwesomeAlertDialog.CUSTOM_IMAGE_TYPE)
        .setTitleText("Sweet!")
        .setContentText("Here's a custom image.")
        .setCustomImage(R.drawable.custom_img)
        .show();

Bind the listener to confirm button???

    new AwesomeAlertDialog(this, AwesomeAlertDialog.WARNING_TYPE)
        .setTitleText("Are you sure?")
        .setContentText("Won't be able to recover this file!")
        .setConfirmText("Yes,delete it!")
        .setConfirmClickListener(new AwesomeAlertDialog.OnSweetClickListener() {
            @Override
            public void onClick(AwesomeAlertDialog sDialog) {
                sDialog.dismissWithAnimation();
            }
        })
        .show();

Show the cancel button and bind listener to it???

    new AwesomeAlertDialog(this, AwesomeAlertDialog.WARNING_TYPE)
        .setTitleText("Are you sure?")
        .setContentText("Won't be able to recover this file!")
        .setCancelText("No,cancel plx!")
        .setConfirmText("Yes,delete it!")
        .showCancelButton(true)
        .setCancelClickListener(new AwesomeAlertDialog.OnSweetClickListener() {
            @Override
            public void onClick(AwesomeAlertDialog sDialog) {
                sDialog.cancel();
            }
        })
        .show();

**Change** the dialog style upon confirming???

    new AwesomeAlertDialog(this, AwesomeAlertDialog.WARNING_TYPE)
        .setTitleText("Are you sure?")
        .setContentText("Won't be able to recover this file!")
        .setConfirmText("Yes,delete it!")
        .setConfirmClickListener(new AwesomeAlertDialog.OnSweetClickListener() {
            @Override
            public void onClick(AwesomeAlertDialog sDialog) {
                sDialog
                    .setTitleText("Deleted!")
                    .setContentText("Your imaginary file has been deleted!")
                    .setConfirmText("OK")
                    .setConfirmClickListener(null)
                    .changeAlertType(AwesomeAlertDialog.SUCCESS_TYPE);
            }
        })
        .show();

[more android tech shares: HMDevCoders](https://github.com/HMDevCoders)

## License

    The MIT License (MIT)

    Copyright (c) 2020 HMDevCoders(https://github.com/HMDevCoders)

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
