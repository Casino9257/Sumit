# Sumit
Instagram 
from selenium import webdriver

driver = webdriver.Chrome(executable_path=r'C:\Users\ME\Local\Google\Chrome\Application\chrome.exe')
driver.maximize_window()
driver.get("http://www.seleniumeasy.com/test/basic-first-form-demo.html")
assert "Selenium Easy Demo - Simple Form to Automate using Selenium" in driver.title

eleUserMessage = driver.find_element_by_id("user-message")
eleUserMessage.clear()
eleUserMessage.send_keys("Test Python")

eleShowMsgBtn=driver.find_element_by_css_selector('#get-input > .btn')
eleShowMsgBtn.click()

eleYourMsg=driver.find_element_by_id("display")
assert "Test Python" in eleYourMsg.text
driver.close()
C:\Users\ME\MyNewEnv\Scripts\python.exe "F:/Sam/TASKS/xings.py"
Traceback (most recent call last):
  File "F:/Sam/TASKS/xings.py", line 3, in <module>
    driver = webdriver.Chrome(executable_path=r'C:\Users\ME\Local\Google\Chrome\Application\chrome.exe')
  File "C:\Users\ME\MyNewEnv\lib\site-packages\selenium\webdriver\chrome\webdriver.py", line 73, in __init__
    self.service.start()
  File "C:\Users\ME\MyNewEnv\lib\site-packages\selenium\webdriver\common\service.py", line 98, in start
    self.assert_process_still_running()
  File "C:\Users\ME\MyNewEnv\lib\site-packages\selenium\webdriver\common\service.py", line 111, in assert_process_still_running
    % (self.path, return_code)
selenium.common.exceptions.WebDriverException: Message: Service C:\Users\ME\Local\Google\Chrome\Application\chrome.exe unexpectedly exited. Status code was: 0


Process finished with exit code 1
