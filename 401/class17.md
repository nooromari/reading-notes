## Web scraping

- **Web scraping** is the process of using bots to extract content and data from a website.

- Unlike screen scraping, which only copies pixels displayed onscreen, web scraping extracts underlying HTML code and, with it, data stored in a database. The scraper can then replicate entire website content elsewhere.


![](https://miro.medium.com/max/1040/0*2QHmHPJxONopybMW.jpg)


1. figure out where we can locate the links to the files we want to download .
2. importing the following libraries:
    ```
    import requests
    import urllib.request
    import time
    from bs4 import BeautifulSoup
    ```
3. set the url to the website and access the site with our requests library.
    ```
    url = 'http://web.mta.info/developers/turnstile.html'
    response = requests.get(url)
    ```
4. parse the html with BeautifulSoup
    ```
    soup = BeautifulSoup(response.text, “html.parser”)
    ```
5. use the method `findAll` to locate all of our `<a>` tags.
    ```
    soup.findAll('a')
    ```
6. extract the actual link that we want. 
    ```
    one_a_tag = soup.findAll('a')[38]
    link = one_a_tag['href']
    ```
7. We can use our urllib.request library to download this file path to our computer. We provide request.urlretrieve with two parameters: file url and the filename. 
    ```
    download_url = 'http://web.mta.info/developers/'+ link
    urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:])
    ```
8. pause our code for a second so that we are not spamming the website with requests. This helps us avoid getting flagged as a spammer.

    ```
    time.sleep(1)
    ```


![](https://res.cloudinary.com/practicaldev/image/fetch/s--caTt0RWA--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/k3qsm22bvhp93x3nbxme.png)