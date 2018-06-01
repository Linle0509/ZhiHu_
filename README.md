# -*- coding: utf-8 -*-
from selenium import webdriver
import time

# 打开网页
browser = webdriver.Chrome()
browser.maximize_window()
browser.get("http://www.zhihu.com/explore")
time.sleep(2)
# 定位登陆按钮
button1=browser.find_element_by_class_name('js-signin-noauth').click()
time.sleep(2)
# 定位账号密码输入框
browser.find_element_by_css_selector('#root > div > main > div > div > div > div.SignContainer-inner > div.Login-content > form > div.SignFlow-account > div.SignFlowInput.SignFlow-accountInputContainer > div.SignFlow-accountInput.Input-wrapper > input').send_keys('15990071864')
browser.find_element_by_css_selector('#root > div > main > div > div > div > div.SignContainer-inner > div.Login-content > form > div.SignFlow-password > div > div.Input-wrapper > input').send_keys('05091818LL~')
# 定位登陆按钮
button2=browser.find_element_by_css_selector('#root > div > main > div > div > div > div.SignContainer-inner > div.Login-content > form > button').click()
time.sleep(2)
browser.find_element_by_id('q').send_keys('2018NBA总决赛')
button3=browser.find_element_by_class_name("sprite-global-icon-magnifier-dark").click()
time.sleep(2)
browser.execute_script('window.scrollBy(0,3000)')
time.sleep(1)

