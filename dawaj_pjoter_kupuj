from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from time import sleep
import time
browser = webdriver.Firefox()
browser.get('https://mi-home.pl/login')
cookie = {'name' : 'ciasteczkko', 'value' : 'czekoladowe'}
browser.add_cookie(cookie)
nazwausera = 'tuwpiszlogin'
haslousera = 'tuwpiszhaslo'
login = browser.find_element_by_xpath("//input[@id='email']")
login.send_keys(nazwausera)
haslo = browser.find_element_by_xpath("//input[@id='passwd']")
haslo.send_keys(haslousera + Keys.RETURN)
sleep(3)
#link mozna zamienic na inny produkt ktory chcemy kupic
browser.get('https://mi-home.pl/inteligentne-urzadzenia/xiaomi-mi-band-4')
do_koszyka = browser.find_element_by_xpath("//button[@class='exclusive']")
do_koszyka.click()
sleep(6)
browser.get('https://mi-home.pl/szybkie-zamowienie')
sleep(10)
wymagane = browser.find_element_by_xpath("//*[@id='customer_newsletter']")
wymagane.click()
regulamin = browser.find_element_by_xpath("//*[@id='gdpr_consent_checkbox']")
regulamin.click()
sleep(10)
paczkomat_arrow = browser.find_element_by_xpath("//span[@class='select2sensbitinpost-selection__arrow']")
paczkomat_arrow.click()
paczkomat_text = browser.find_element_by_xpath("/html/body/span/span/span[1]/input")
paczkomat_text.send_keys("WRO01M")
sleep(5)
paczkomat_text.send_keys(Keys.RETURN)
blik = browser.find_element_by_xpath("//*[@for='module_payment_200_1']")
blik.click()
