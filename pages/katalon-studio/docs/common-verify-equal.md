---
title: "[Common] Verify Equal" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/common-verify-equal.html 
description: 
---
Description 
------------

Verify if two objects are equal. 

Parameters 
-----------

<table class="wrapped relative-table confluenceTable" style="width: 87.1552%;"><colgroup><col style="width: 11.2217%;"><col style="width: 10.9502%;"><col style="width: 8.50679%;"><col style="width: 69.3213%;"></colgroup><tbody><tr class="xtr-0"><th class="xtd-0-0 confluenceTh">Param</th><th class="xtd-0-1 confluenceTh">Param Type</th><th class="xtd-0-2 confluenceTh" colspan="1">Mandatory</th><th class="xtd-0-3 confluenceTh" colspan="1">Description</th></tr><tr class="xtr-1"><td class="xtd-1-0 confluenceTd" colspan="1"><span style="color: rgb(0,0,0);">actualObject&nbsp;</span></td><td class="xtd-1-1 confluenceTd" colspan="1"><span style="color: rgb(0,0,0);">Object&nbsp;</span></td><td class="xtd-1-2 confluenceTd" colspan="1">Required</td><td class="xtd-1-3 confluenceTd" colspan="1"><span style="color: rgb(0,0,0);">Represent the actual object.</span></td></tr><tr class="xtr-2"><td class="xtd-2-0 confluenceTd" colspan="1"><span style="color: rgb(0,0,0);">expectedObject&nbsp;</span></td><td class="xtd-2-1 confluenceTd" colspan="1"><span style="color: rgb(0,0,0);">Object&nbsp;</span></td><td class="xtd-2-2 confluenceTd" colspan="1">Required</td><td class="xtd-2-3 confluenceTd" colspan="1"><span style="color: rgb(0,0,0);">Represent the expected object.</span></td></tr><tr class="xtr-3"><td class="xtd-3-0 confluenceTd"><span style="color: rgb(0,0,0);">flowControl</span></td><td class="xtd-3-1 confluenceTd"><span style="color: rgb(0,0,0);">FailureHandling</span></td><td class="xtd-3-2 confluenceTd" colspan="1">Optional</td><td class="xtd-3-3 confluenceTd" colspan="1"><span style="color: rgb(0,0,0);">Spec</span><span>ify </span><a href="https://docs.katalon.com/x/qAAM" rel="nofollow">failure handling</a><span> schema to determine whether the execution should be allowed to continue or stop.</span></td></tr></tbody></table>

Returns
-------

<table class="wrapped confluenceTable"><colgroup><col><col></colgroup><tbody><tr class="xtr-0"><th class="xtd-0-0 confluenceTh">Param Type</th><th class="xtd-0-1 confluenceTh">Description</th></tr><tr class="xtr-1"><td class="xtd-1-0 confluenceTd"><span style="color: rgb(0,0,0);">Boolean</span></td><td class="xtd-1-1 confluenceTd"><ul><li><p><span style="color: rgb(0,0,0);"><strong>true</strong>&nbsp;if the actual number and the expected number are equal.</span></p></li><li><p><span style="color: rgb(0,0,0);"><strong>false</strong>&nbsp;if the actual number and the expected number are NOT equal.</span></p></li></ul></td></tr></tbody></table>

Example 
--------

You want to verify if two given numbers are equal.

*   Manual view    
    ![](../../images/katalon-studio/docs/common-verify-equal/image2017-3-3 17_10_11.png)
*   Script view 
    
    ```groovy
    import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
    import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
    import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
    import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
    import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
    import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
    import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
    import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
    import com.kms.katalon.core.model.FailureHandling as FailureHandling
    import com.kms.katalon.core.testcase.TestCase as TestCase
    import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
    import com.kms.katalon.core.testdata.TestData as TestData
    import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
    import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
    import com.kms.katalon.core.testobject.TestObject as TestObject
    import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
    import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
    import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
    import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
    import internal.GlobalVariable as GlobalVariable
    
    'Use WebUI keyword'
    WebUI.verifyEqual(10, 10)
     
    'Use Mobile keyword'
    Mobile.verifyEqual(10, 10)
     
    'Use WS keyword'
    WS.verifyEqual(10, 10)
    
    ```