---
title: "Spy Mobile Utility" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/spy-mobile-utility.html 
description: 
---
Capture objects using Spy Mobile Utility
----------------------------------------

Before capturing test objects on the mobile application, make sure that you have successfully configured the environment for mobile testing. Refer to [Before You Start](/display/KD/Before+You+Start) for more details.

1.  Connect the mobile device to your PC.  
      
    
2.  Click on the **Spy Moble Utility** button from the main toolbar.  
    ![](../../images/katalon-studio/docs/spy-mobile-utility/image2017-2-23 14_15_42.png)  
      
    
3.  The **Spy Mobile Utility** dialog is displayed. Specify the settings of your mobile testing in **Configurations** section.   
    ![](../../images/katalon-studio/docs/spy-mobile-utility/image2017-8-24 15_9_28.png)
    
    Where:
    
    <table class="relative-table wrapped confluenceTable" style="width: 51.2676%;"><colgroup><col style="width: 23.2123%;"><col style="width: 76.7877%;"></colgroup><tbody><tr class="xtr-0"><th class="xtd-0-0 confluenceTh">Field</th><th class="xtd-0-1 confluenceTh">Description</th></tr><tr class="xtr-1"><td class="xtd-1-0 confluenceTd">Device Name</td><td class="xtd-1-1 confluenceTd">The smartphone to capture objects from. All of your connected devices should be displayed in this list.</td></tr><tr class="xtr-2"><td class="xtd-2-0 confluenceTd">Application Type</td><td class="xtd-2-1 confluenceTd">Currently, Katalon Studio only support native mobile applications.</td></tr><tr class="xtr-3"><td class="xtd-3-0 confluenceTd">Application File</td><td class="xtd-3-1 confluenceTd">The absolute path to your mobile application file (<strong>.apk</strong> file for Android or <strong>.ipa</strong> file for iOS).</td></tr></tbody></table>
    
    Click **Start** when you're done with the settings.
    
4.  The specified mobile application will be deployed and opened on the real device.   
      
    
5.  The **Device View** dialog is displayed to show the current screenshot of your real device.   
    All the mobile objects from that screenshot are analyzed and organized in a **hierarchical view** which could be found at **All Objects** section of the **Spy Mobile Utility** dialog.  
    Click on any object from the **hierarchical view** and it is highlighted in **Device View** accordingly.  
    ![](../../images/katalon-studio/docs/spy-mobile-utility/image2017-8-24 15_22_48.png)  
      
    
6.   Select any objects from the **hierarchical view** and click **Add to Object Repository** to save them to Katalon Studio.  
    ![](../../images/katalon-studio/docs/spy-mobile-utility/image2017-1-23 17_17_48.png)  
      
    
7.  The **Folder Browser** dialog is prompted to decide where to save the captured objects. Select your preferred location then click **OK**.  
    ![](../../images/katalon-studio/docs/spy-mobile-utility/image2017-1-23 17_20_41.png)  
      
    
8.  The captured objects will be added to **Object Repository** accordingly.  
    ![](../../images/katalon-studio/docs/spy-mobile-utility/image2017-1-24 10_57_32.png)  
      
    
9.  You can continue with the current mobile screen or navigate to other interfaces as needed. To reload the **Device View** as well as the details in **Spy Mobile Utility**, simply click on the **Capture Object** button.  
    ![](../../images/katalon-studio/docs/spy-mobile-utility/image2017-1-23 17_0_31.png)  
      
    
10.  Close the **Spy Mobile Utility** dialog when you're done with capturing objects.