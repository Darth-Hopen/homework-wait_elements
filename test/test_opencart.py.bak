from selenium.webdriver.common.by import By
from selenium.webdriver.support.wait import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC


def test_product_page(browser):
    browser.get(url=browser.url + "/index.php?route=product/category&path=20")
    wait = WebDriverWait(driver=browser, timeout=2)
    wait.until(EC.presence_of_all_elements_located((By.CSS_SELECTOR, ".product-grid img")))

    browser.find_element(By.CSS_SELECTOR, ".list-group .active")
    browser.find_element(By.XPATH, "//label[text()='Sort By:']")
    browser.find_element(By.XPATH, "//button//span[text()='Add to Cart']")
    browser.find_element(By.XPATH, "//div/div[contains(text(), 'Showing')]")
    browser.find_element(By.XPATH, "//button/span[text()= 'Currency']/ancestor::button")


def test_login_page(browser):
    browser.get(url=browser.url + "/admin")
    wait = WebDriverWait(driver=browser, timeout=2)
    wait.until(EC.presence_of_element_located((By.CLASS_NAME, "panel-default")))

    browser.find_element(By.ID, "input-username")
    browser.find_element(By.NAME, "password")
    browser.find_element(By.CSS_SELECTOR, "button[type='submit']")
    browser.find_element(By.LINK_TEXT, "Forgotten Password")
    browser.find_element(By.XPATH, "//*[text()='OpenCart']")


def test_main_page(browser):
    browser.get(url=browser.url)
    wait = WebDriverWait(driver=browser, timeout=2)
    wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".navbar-collapse")))

    browser.find_element(By.CSS_SELECTOR, "a[title='My Account'] span.hidden-xs")
    browser.find_element(By.NAME, "search")
    browser.find_element(By.CSS_SELECTOR, ".btn-inverse")
    browser.find_element(By.LINK_TEXT, "Your Store")
    browser.find_element(By.CSS_SELECTOR, ".product-layout")


def test_product_page(browser):
    browser.get(url=browser.url + "/index.php?route=product/product&product_id=43")
    wait = WebDriverWait(driver=browser, timeout=2)
    wait.until(EC.presence_of_all_elements_located(
        (By.CSS_SELECTOR, "input[name='product_id'] ~ button")
    ))

    browser.find_element(By.CSS_SELECTOR, ".breadcrumb a")
    browser.find_element(By.CSS_SELECTOR, ".image-additional")
    browser.find_element(By.CSS_SELECTOR, ".active > a")
    browser.find_element(By.CSS_SELECTOR,
                         ".btn-group > button[data-original-title='Add to Wish List']")
    browser.find_element(By.CSS_SELECTOR, "[name='quantity']")


def test_product_page(browser):
    browser.get(url=browser.url + "/index.php?route=account/register")
    wait = WebDriverWait(driver=browser, timeout=2)
    wait.until(EC.title_is("Register Account"))

    browser.find_element(By.CSS_SELECTOR, "aside > div.list-group")
    browser.find_element(By.CSS_SELECTOR, "fieldsets#account")
    browser.find_element(By.CSS_SELECTOR, "[name='firstname']")
    browser.find_element(By.LINK_TEXT, "Privacy Policy")
    browser.find_element(By.CSS_SELECTOR, "[value='1'][name='newsletter']")
    browser.find_element(By.CSS_SELECTOR, "[value='Continue']")
