[id=num1.py](https://github.com/user-attachments/files/23857438/id.num1.py)stepik_auto_tests_course/

[README.md.txt](https://github.com/user-attachments/files/23857247/README.md.txt)
[Uploading REAРепозиторий для выполнения заданий по курсу Stepik:
«Автоматизация тестирования с помощью Selenium и Python».

Здесь находятся решения заданий и примеры кода.DME.md.txt…]()
[Uploadfrom selenium import webdriver
from selenium.webdriver.common.by import By
import time 

link = "http://suninjuly.github.io/execute_script.html"

browser = webdriver.Chrome()
browser.get(link)

try:
    num1_el = browser.find_element(By.ID, "num1")
    num1_text = num1_el.text

    num2_el = browser.find_element(By.ID, 'num2')
    num2_text = num2_el.text
    
    result = int(num1_text) + int(num2_text)
    result_str = str(result)

    option = browser.find_element(By.CSS_SELECTOR, f"[value='{result_str}']")
    option.click()
   

    submit = browser.find_element(By.CSS_SELECTOR, "button.btn")
    submit.click()


finally:
    time.sleep(10)
    browser.quit()ing id=num1.py…]()
