[Telegram](https://telegram.org) (see official [FAQ](https://telegram.org/faq) and [wikipedia](https://en.wikipedia.org/wiki/Telegram_(messaging_service)) is developing Telegram Open Network (TON) (see list.[wiki](https://list.wiki/Telegram_Open_Network_(TON) and wikipedia.[ru](https://ru.wikipedia.org/wiki/Telegram_Open_Network)), centered around a new generation (and [[high performance DLs|high performance]]) [[blockchain]] project. TON is envisioned to support for decentralised applications and [[smart contract]]s, distributed file-storage service (TON Storage), micropayments, a proxy service (TON proxy) and TON DNS. TON had large private ICO for large investors in early 2018 and is supposed to be fully operational in Q4 2019. According to press ([kod.ru](https://kod.ru/ton-test-version-apr-2019), [zfr.su](https://zfr.su/nachalsya-zakrytyy-beta-test-telegram-open-network), [cryptor.net](https://cryptor.net/news/pavel-durov-zapustil-testnet-telegram-open-network-3490), [beincrypto](https://beincrypto.com/telegram-launches-open-network-testnet-in-private-beta/), [kryptonews](https://www.kryptonews.org/2019/04/12/telegram-launches-open-network-testnet-in-private-beta), [other](https://ton-telegram.net/news/testnet-launched)), TON testnet has started, with access only to limited parties, on April 11, 2019. Due
SEC suit in US the original project has been discontinued in mid 2020. Some partial replica of original vision, building on available early 2020 TON software are being developed as FreeTON project. The SEC court proceedings are studied case in the paper 

* Muisala et al., _Telegram: deconstructing one of the biggest blockchain cases of 2020_, [doi](https://doi.org/10.1108/JOIC-10-2020-0035)

Official announcement of halt of the project is

* Pavel Durov, [What was TON and why it is over](https://telegra.ph/What-Was-TON-And-Why-It-Is-Over-05-12)

TON blockchain's native cryptocurrency for original net was called Gram. The underlying blockchain protocol supports a number of innovative ideas helping scaling, including notably infinite sharding paradigm and instant hypercube routing. It employs a new [[virtual machine]] (TON VM), supporting algebraic types. TON has upgradeable  formal  blockchain  specifications and support for off-chain payment networks.

* TON whitepaper, 23 page [pdf](https://cdn.crowdfundinsider.com/wp-content/uploads/2018/03/TON-White-Paper-Telegram-ICO.pdf), mirrors [pdf](https://drive.google.com/file/d/1ucUeKg_NiR8RxNAonb8Q55jZha03WC0O/view) [pdf](https://icorating.com/upload/whitepaper/gNQ7e9z3lCGi519Wz8mmC0Kg8aA0goeZKAQ802vo.pdf)
* [[nlab:Nikolai Durov]]'s 132-page technical overview _Telegram Open Network_, Dec 2017 [pdf](https://toncoin.tech/TON-official-whitepaper.pdf), mirror [pdf](https://www.kriptovaluta.hr/wp-content/uploads/2018/03/TON-Technology.pdf); _Telegram Open Network Blockchain_, Sep 2018, 121 pp. [pdf](https://www.docdroid.net/qY4sQEv/telegram-open-network-blockchain-september-5-2018.pdf); _Telegram Open Network Virtual Machine_, Sep. 2018, 148 pp. [pdf](https://www.docdroid.net/R3vEKBY/telegram-open-network-virtual-machine-september-5-2018.pdf); _Catchain consensus: an outline_, [pdf](https://test.ton.org/catchain.pdf)

The whole thing will run on protocols used already by Telegram and use similar specs:

* specs: [TL language](https://core.telegram.org/mtproto/TL) ("Type Language", TON will use an upgrade, TL-B), [MTProto mobile protocol](https://core.telegram.org/mtproto)
* JAVA MTProto implementation [github](https://github.com/ex3ndr/telegram-mt)
* github [OpenTl.ClientApi](https://opentl.github.io/OpenTl.ClientApi), [mtproto2json](https://github.com/nikat/mtproto2json)

It will use Telegram Passport.

* Telegram Passport [manual](https://core.telegram.org/passport), [example](https://core.telegram.org/passport/example), [telepass.me](https://telepass.me), [guide](https://technandu.com)

> Telegram is introducing a new feature called Passport, a single sign-on option for services that need actual real-world IDs or documents. Passport will let users store their files and data in Telegram's cloud and pass it directly on to services that need that information (via Neowin).

See also [[digital identity]].

According to a press release [pdf](https://www.wirecard.com/uploads/tx_nenews/PM_2019_04_17_EN_TON_01.pdf) (accompanying event of partnership with Wirecard), 

> [TON Labs](https://tonlabs.io) is a core infrastructure and ecosystem developer for TON (Telegram Open Network). Its secure and accessible TON.Dev and TON.Space environments will deliver a TON full node implementation, a versatile toolchain and a cutting-edge SDK, as well as novel ways users interact with fintech services. It will enable the developer community to create, deploy, distribute and manage TON chains for consumer and enterprise applications.

According to other [press](https://www.vedomosti.ru/technology/articles/2019/04/03/798189-razrabotchikam-uprostyat-sozdanie-prilozhenii), TON Labs developes their tools using technical documentation which Telegram distributed to their investors in Autumn 2019, but may also have other insider information making pre-release development effective.

[[!redirects TON]]