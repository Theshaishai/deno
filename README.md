character.ai

功能：ai聊天
    1. 你为什么觉得这个功能最有价值：
此功能是用户体验中的一大功能，用户最直接的体验就是与AI展开对话，此对话是决定了用户对这个网站的兴趣度
    2. 这个功能所需要测试点有哪些，罗列出来：
一：UI界面
    1，对界面与PRO进行对比查看是否有误差
    2，UI界面字体，模块颜色是否一致
    3，界面是否整洁有序
二：功能
    1，聊天界面输入框包含：各国语言输入，敏感输入，字母，特殊符号，空格，输入字符串的长度边界值
    2，输入框右侧纸飞机图标点击测试，输入文字后点击，无文字时点击，AI会话未结束时点击发送文字
    3，输入框右侧发送按钮旁放大缩小调整按钮
    4，输入框输入非数据库内容，比如“翻译星期8”
    5，让AI输出语音文件，视频文件，图片
    6，左上角点赞按钮，点赞是否成功且数字增加，取消点赞数字减少，连续点击数字是否为最终点赞或是取消按钮
    7，点击“踩”按钮是否成功点亮图标，取消踩按钮置灰（此处点赞显示数量，踩未显示数量）
    8，左上角返回按钮，点击后是否返回上一页
    9，AI输出聊天文字是否可以复制粘贴
   10，AI输出聊天内容可以评价，可以选择几颗星星，查看星星是否点亮颜色高亮显示，以及文字显示是否正确
   11，AI输出内容可以评价上传，上传可以备注文字，备注的文字有无限制长度，类型
   12，评价内容点击提交按钮可以提交内容，有防连点击功能（此处备注内容无法提交，报错500）
   13，内容有取消按钮，可以取消上传
三：性能
    1，点击AI跳转至聊天界面的的响应时间
    2，打开此网址到网页渲染完成的响应时间
    3，聊天界面AI会话时间的响应时间
    4，输入框输入内容到发送出去的响应时间
    5，聊天界面返回的响应时间
    6，网站内的点击，跳转响应时间
    7，服务器性能
四，兼容性测试
     1，WEB端：国外不同浏览器，如：谷歌，edg等等
     2，PC端：WINDOWS，MAC，PC端APP版本，下载，安装，卸载，更新
     3，手机端APP：不同手机，安卓（华为，谷歌，三星，小米等等）和苹果（不同的型号，不同的IOS版本），软件的下载，安装，更新，卸载






class PC():
    def denglu(self):
        from selenium import webdriver                      # 从selenium调用web驱动器
        import time                                         # 调用时间
        import os
        from selenium.webdriver.common.by import By         #
        from selenium.webdriver import Keys                 # 导入键盘包
        from selenium.webdriver import Keys, ActionChains   # 导入鼠标包
        driver = webdriver.Chrome()  # 驱动的路径
        driver.maximize_window()                            # 窗口最大化
        # driver.minimize_window()                          #窗口最小化

        driver.get("https://beta.character.ai/")
        time.sleep(10)
        # 登录账号密码
        driver.find_element(By.XPATH, '').clear()
        driver.find_element(By.XPATH, '').clear()
        time.sleep(2)
        driver.find_element(By.XPATH, '').send_keys()
        driver.find_element(By.XPATH, '').send_keys("")
        driver.find_element(By.XPATH,'').click()
        time.sleep(2)

P=PC
P.denglu(1)

