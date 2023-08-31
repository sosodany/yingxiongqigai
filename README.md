# yingxiongqigai
def odbcreatefile():
    handles = driver.window_handles
    driver.switch_to.window(handles[1])
    wait.until(EC.visibility_of_element_located((By.XPATH, '//div[@aria-label="文件夹路径 必需"]'))).send_keys("/邮件列表pa存储")
    time.sleep(2)
    wait.until(EC.visibility_of_element_located((By.XPATH, '//div[@aria-label="文件名"]'))).click()
    time.sleep(2)
    driver.find_element(By.XPATH,"//div[@class='msla-token-picker-option-title' and text()='当前时间']").click()
    time.sleep(1)
    wait.until(EC.visibility_of_element_located((By.XPATH, '//div[@aria-label="文件名"]'))).send_keys(".csv")
    time.sleep(2)
    wait.until(EC.visibility_of_element_located((By.XPATH, '//div[@aria-label="文件内容"]'))).click()
    time.sleep(2)
    driver.find_element(By.XPATH,"//div[@class='msla-token-picker-option-title' and text()='输出']").click()
    time.sleep(3)

    driver.find_element(By.XPATH,"//button[contains(text(),'保存')]").click()
    wait.until(EC.visibility_of_element_located((By.XPATH, "//*[contains(text(), '您的流已准备就绪')]")))
