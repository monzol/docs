---
title: "[WebUI] Verify Option Present By Label" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-verify-option-present-by-label.html 
description: 
---
Description
-----------

Verify if the option with the given displayed text does exist.

![](../../images/katalon-studio/docs/webui-verify-option-present-by-label/label.jpg)

Parameters
----------

<table class="wrapped confluenceTable"><colgroup><col><col><col><col></colgroup><tbody><tr class="xtr-0"><th class="xtd-0-0 confluenceTh">Param</th><th class="xtd-0-1 confluenceTh">Param Type</th><th class="xtd-0-2 confluenceTh" colspan="1">Mandatory</th><th class="xtd-0-3 confluenceTh" colspan="1">Description</th></tr><tr class="xtr-1"><td class="xtd-1-0 confluenceTd" colspan="1">to</td><td class="xtd-1-1 confluenceTd" colspan="1">TestObject</td><td class="xtd-1-2 confluenceTd" colspan="1">Required</td><td class="xtd-1-3 confluenceTd" colspan="1">Represent a web element.</td></tr><tr class="xtr-2"><td class="xtd-2-0 confluenceTd" colspan="1">label</td><td class="xtd-2-1 confluenceTd" colspan="1">String</td><td class="xtd-2-2 confluenceTd" colspan="1">Required</td><td class="xtd-2-3 confluenceTd" colspan="1">Displayed texts of the options to be verified if existing.</td></tr><tr class="xtr-3"><td class="xtd-3-0 confluenceTd" colspan="1">isRegex</td><td class="xtd-3-1 confluenceTd" colspan="1">boolean</td><td class="xtd-3-2 confluenceTd" colspan="1">Required</td><td class="xtd-3-3 confluenceTd" colspan="1">True if the label is a regular expression, false by default.</td></tr><tr class="xtr-4"><td class="xtd-4-0 confluenceTd" colspan="1">timeout</td><td class="xtd-4-1 confluenceTd" colspan="1">int</td><td class="xtd-4-2 confluenceTd" colspan="1">Required</td><td class="xtd-4-3 confluenceTd" colspan="1">System will wait at most timeout (seconds) to return the result.</td></tr><tr class="xtr-5"><td class="xtd-5-0 confluenceTd"><span style="color: rgb(0,0,0);">flowControl</span></td><td class="xtd-5-1 confluenceTd"><span style="color: rgb(0,0,0);">FailureHandling</span></td><td class="xtd-5-2 confluenceTd" colspan="1">Optional</td><td class="xtd-5-3 confluenceTd" colspan="1"><span style="color: rgb(0,0,0);">Spec</span>ify <a href="https://docs.katalon.com/x/qAAM" rel="nofollow">failure handling</a> schema to determine whether the execution should be allowed to continue or stop</td></tr></tbody></table>

Returns
-------

<table class="wrapped confluenceTable"><colgroup><col><col></colgroup><tbody><tr class="xtr-0"><th class="xtd-0-0 confluenceTh">Param Type</th><th class="xtd-0-1 confluenceTh" colspan="1">Description</th></tr><tr class="xtr-1"><td class="xtd-1-0 confluenceTd" colspan="1">boolean</td><td class="xtd-1-1 confluenceTd" colspan="1"><ul><li><strong>true:</strong>&nbsp;if options with given displayed text is present.</li><li><strong>false:</strong>&nbsp;if options with given displayed text do NOT present</li></ul></td></tr></tbody></table>

Example
-------

You want to verify if 'HongKong Cura Health Center' does present in the list.

```groovy
import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
import internal.GlobalVariable as GlobalVariable
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS

'Open browser and navigate to demo AUT site.'
WebUI.openBrowser(GlobalVariable.G_SiteURL)

'Click on \'Book Appointment\' button'
WebUI.click(findTestObject('Page_CuraHomepage/btn_MakeAppointment'))

'Verify \'HongKong Cura Health Center\' option in \'Facility\' list is present'
WebUI.verifyOptionPresentByLabel(findTestObject('Page_CuraAppointment/lst_Facility'), 'HongKong Cura Health Center', 
    false, 20)

'Close browser'
WebUI.closeBrowser()
```