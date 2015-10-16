# net-curl

## Fase start

    $curl = new curl();
    $curl->prepare('https://github.com');
    $content = $curl->execute();


## Some tricks

    $curl = new curl();
    $curl->useProxy('1.2.3.4:3128', 'http');
    $curl->setConnectionTimeout(10);
    $curl->setTimeout(15);
    $curl->setCookieFile('/custom/cookie/file');
    $curl->addOptions([
        CURLOPT_USERAGENT => 'Opera/9.80 (X11; Linux i686; Ubuntu/14.10) Presto/2.12.388 Version/12.16'
    ]);
    $curl->prepare('https://github.com/search', ['q' => 'InfoStars LLC', 'type' => 'Users')
    $content = $curl->execute();

Enjoy!