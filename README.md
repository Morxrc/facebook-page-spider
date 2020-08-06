# facebook-page-spider (crawler)
Facebook 模拟账号登陆根据目标用户的 facebook id 爬取页面数据，基于 Python + Helium (比Selenium更轻量) ，非 facebook develop api 方法。 另注：有被封账号的风险，仅供参考和学习!

## Features：
1. 根据facebook用户id进行多用户的数据爬取
2. 可设置代理（国内翻墙）
3. 获取帖子信息
4. 消除chrome消息弹窗
5. 筛选评论（当前暂被注释掉）

## Usage：
所需环境：Python3、Chrome浏览器
1. 安装 Helium: `pip install helium`
2. 下载与chrome浏览器对应版本的chromedriver，放到python环境path下（或其他系统环境path下）：http://chromedriver.storage.googleapis.com/index.html
3. 定制 `crawler.py` 文件属性:
    - **PAGE_URL**: Facebook页面的url（默认为读取facebook_id.txt中每个id对应的页面url）
    - **SCROLL_DOWN**: 加载帖子向下滚动的次数
    - **FILTER_CMTS_BY**: 通过以下方式展示评论 `MOST_RELEVANT` / `NEWEST` / `ALL_COMMENTS`
    - **VIEW_MORE_CMTS**: 加载更多评论的次数
    - **VIEW_MORE_REPLIES**: 加载更多回复的次数
4. 在load_page.py中设置自己登陆facebook的邮箱和密码：`YOUR_EMAIL`；`YOUR_PASSWORD`
5. 开始爬虫: `python crawler.py`

注：如果不想显示chromedriver浏览器，将load_page.py中的`start_chrome()`方法中的`headless`置为True

## Reference:
* https://github.com/18520339/facebook-crawling
* https://github.com/mherrmann/selenium-python-helium
* https://my.oschina.net/seeseven/blog/2125271
* https://blog.csdn.net/andydufre/article/details/79204158
* https://github.com/mherrmann/selenium-python-helium/blob/master/helium/__init__.py

> 另附上该代码本人博客的网址:  
