
<h1>Chrome</h1>
  options = ChromeOptions()
  driver = webdriver.Chrome(options=options)
  
  driver.quit()
  

<h2>Start the session</h2>
 driver = webdriver.Chrome()
 
<h2>Take action on browser</h2>
 driver.get("https://google.com")
  
<h2>Request browser information</h2>
 title = driver.title
 
<h2>Establish Waiting Strategy</h2>
 driver.implicitly_wait(0.5)
 - If you want to make sure that the element is on the page before you attempt to locate it and the element is in an interactable state before you attempt to interact with it.

<h2>Find an element</h2>
search_box = driver.find_element(by=BY.NAME, value="q")
search_button = driver.find_element(by=By.NAME, value="btnk")

<h2>Take action on element</h2>
search_box.send_keys("Selenium")
search_button.click()

<h2>Request element information</h2>
value = search_box.get_attribute("value")

<h2>End the session</h2>
driver.quit()





<h2>Code</h2>
<pre><code>from selenium import webdriver
from selenium.webdriver.common.by import By
<br><br>
def test_eight_components():

    driver = webdriver.Chrome()
    driver.get("https://google.com")

    title = driver.title
    assert title == "Google"

    driver.implicitly_wait(0.5)

    search_box = driver.find_element(by=By.NAME, value="q")
    search_button = driver.find_element(by=By.NAME, value="btnK")

    search_box.send_keys("Selenium")
    search_button.click()

    search_box = driver.find_element(by=By.NAME, value="q")
    value = search_box.get_attribute("value")
    assert value == "Selenium"

    driver.quit()
</code>
</pre>


