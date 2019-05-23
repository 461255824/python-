# python-人脸识别
- openvc-python
手机连接小米6 自动点赞
desired_caps = {}
        desired_caps['automationName'] = "uiautomator2"
        desired_caps['platformName'] = 'Android'
        desired_caps['platformVersion'] = '8.0.0'
        desired_caps['deviceName'] = '9b19913a'
        # 使用 Unicode 输入法
        desired_caps['unicodeKeyboard'] = True
        # 重置输入法到原有状态
        desired_caps['resetKeyboard'] = False
        desired_caps['noReset'] = True
        desired_caps['appPackage'] = 'com.ss.android.ugc.aweme'
        # desired_caps['app'] = 'F:// debug.apk'
        desired_caps['appActivity'] = '.main.MainActivity'
        self.driver = webdriver.Remote('http://localhost:4723/wd/hub', desired_caps)
print('开启程序')
        time.sleep(3)
        # 检测是否有用户隐私弹框com.ss.android.ugc.aweme:id/s3
        try:
            secrect = self.driver.find_element_by_id('com.ss.android.ugc.aweme:id/s3').click()
        except Exception:
            pass
        # 权限设定
        self.driver.find_element_by_id('android:id/button1').click()
        self.driver.find_element_by_id('android:id/button1').click()
        time.sleep(3)
        # self.driver.find_element_by_id('com.ss.android.ugc.aweme:id/s3').click()
        self.driver.find_element_by_id('com.ss.android.ugc.aweme:id/buu').click()
        # self.driver.swipe(500, 1200, 500, 800, 100)
        time.sleep(3)
        self.driver.tap([(500, 500)])

        # 登录
        # 点击（980，930）爱心调转到登录
        print("点击（980，930）爱心调转到登录")
        time.sleep(2)
        self.driver.tap([(980, 930)])
        # 点击（940，150）使用密码登录
        time.sleep(2)
        self.driver.tap([(940, 150)])
        # 输入账户com.ss.android.ugc.aweme:id/am9 13917862359
        time.sleep(2)
        self.driver.find_element_by_id('com.ss.android.ugc.aweme:id/am9').send_keys("13917862359")
        # 输入密码com.ss.android.ugc.aweme:id/aqb yqy1990102
        self.driver.find_element_by_id('com.ss.android.ugc.aweme:id/aqb').send_keys("yqy1990102")
        # 选择同意协议	com.ss.android.ugc.aweme:id/dcd
        self.driver.find_element_by_id('com.ss.android.ugc.aweme:id/dcd').click()
        time.sleep(2)
        # 点击同意登录	com.ss.android.ugc.aweme:id/ly
        time.sleep(2)
        self.driver.find_element_by_id('com.ss.android.ugc.aweme:id/ly').click()
        time.sleep(5)
        # # 验证码
        # code  = identifyingCode(self.driver,254,763,800,950).replace(" ","")
        # while code =="" or len(code) != 4:
        #     code = identifyingCode(self.driver, 254, 763, 800, 950).replace(" ","")
        # print("验证码"+code)
        time.sleep(5)
        for i in range(1, 1000):
            # 点击爱心
            time.sleep(3)
            self.driver.tap([(980, 930)])
            time.sleep(1)
            print("点赞：" + str(i) + "个视频")
            self.driver.swipe(500, 1200, 500, 600, 200)
