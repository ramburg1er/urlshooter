from html2image import Html2Image
from multiprocessing.dummy import Pool as ThreadPool

def take_screenshot(url):
    hti = Html2Image()
    url_name = url.replace('\n', '')
    if '//' in url_name:
        url_name = url_name.split('//')[1]
    url_name = url_name + ".png"
    hti.screenshot(url=url,save_as=str(url_name))
    print('[+] Scanned:', url)

def main():
    urls_path = str(input("Enter urls file path: "))
    f = open(urls_path, "r")
    urls = f.readlines()
    urls_count = len(urls)
    pool = ThreadPool(15)
    results = pool.map(take_screenshot,urls)

if __name__ == "__main__":
    main()






