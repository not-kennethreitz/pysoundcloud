PySoundCloud
============

SoundCloud is a single–page webapp (all content served via JavaScript).

This repo serves as an experiment to see how to scrape and parse a website
like this using `requests-html <http://html.python-requests.org>`_, which
features a full web browser for scraping such websites.

Usage
=====

.. code-block:: pycon

    >>> from pysoundcloud import SoundCloud
    >>> sc = SoundCloud()

    >>> kenneth = sc.get_user('infinitestate')
    >>> kenneth.meta
    {'username': 'Infinite State (Kenneth Reitz)Monthly Pro Unlimited plan', 'additional': 'Kenneth Reitz', 'bio': 'Wandering musician, idealist, and moral fallibilist. Simplicity is always better than functionality.\nkennethreitz.org/music', 'followers': 1323, 'following': 250, 'tracks': 485, 'likes': 81}

    >>> kenneth.following
    [<User 'squadpack'>, <User 'thenoiseunion'>, <User 'theartistunion'>, <User 'user-515843919'>, <User 'user-509329189'>, <User 'jnicolaisen'>, <User 'doug-reitz'>, <User 'paintingfishes'>, <User 'mdzcloud'>, <User 'wingsofsunshine'>, <User 'nasa'>, <User 'rplktr'>, <User 'ywcbropher'>, <User 'hamburgerhelper'>, <User 'funka7ron'>, <User 'kanyewest'>, <User 'sasha-rosser'>, <User 'middle-room'>, <User 'madonna'>, <User 'greenday'>, <User 'aerosmith'>, <User 'qotsa'>, <User 'radiohead'>, <User 'jimihendrix'>, <User 'foofighters'>, <User 'tenaciousd'>, <User 'matt-lawless-3'>, <User 'syntheticreality'>, <User 'heddle317'>, <User 'lemonjuice91'>, <User 'nihiti'>, <User 'eva_jade'>, <User 'octobersveryown'>, <User 'obamawhitehouse'>, <User 'ramdass'>, <User 'demianson'>, <User 'kimthera4444'>, <User 'henry-campbell-7'>, <User 'stephanie-moran-mangino'>, <User 'nrrb'>, <User 'geraldrich'>, <User 'jasonamyers'>, <User 'lance-roggendorff'>, <User 'import-this'>, <User 'umemusic'>, <User 'buddhify'>, <User 'rob-dehaven'>, <User 'beshr'>, <User 'montylounge'>, <User 'kay-louise-2'>, <User 'cody-soyland'>, <User 'moby'>, <User 'johnmangino'>, <User 'tetelestaiband'>, <User 'justinabrahms'>, <User 'enneff'>, <User 'dkeithrobinson'>, <User 'lindseystomp'>, <User 'erik'>, <User 'audreyrg'>, <User 'kevnull'>, <User 'podcastmaster'>, <User 'swillison'>, <User 'bjarni-ingimar-j-l-usson'>, <User 'bryon-roche'>, <User 'nate-aune'>, <User 'timoni-west'>, <User 'florian-le-goff'>, <User 'austin-bales'>, <User 'ola-sitarska'>, <User 'tsykoduk'>, <User 'regebro'>, <User 'lukasz-langa'>, <User 'mtrifiro-duplicate'>, <User 'mtrifiro'>, <User 'amrithap'>, <User 'pythonchelle'>, <User 'timoni'>, <User 'rsms'>, <User 'jonathanchu'>, <User 'wburnd'>, <User 'teralaser'>, <User 'wayne-werner'>, <User 'taurus-olson'>, <User 'andrew-danger-pennebaker'>, <User 'kyle-boyer-5'>, <User 'nineinchnails'>, <User 'mad-zach'>, <User 'arcseconds'>, <User 'stephentayler'>, <User 'leigh-bauserman'>, <User 'glenn-gillen'>, <User 'brian-stoepker'>, <User 'benjamin-warfield-smith'>, <User 'mtt2p'>, <User 'harold-bonneville'>, <User 'heather-b-duthie'>, <User 'yoav-lurie'>, <User 'jfranusic'>, <User 'evajlandon'>, <User 'evablackmer8902'>, <User 'fivelights'>, <User 'simon-segfault'>, <User 'craig-slusher'>, <User 'gusanlyon'>, <User 'anoemi'>, <User 'kirby-ferguson'>, <User 'elizabeth-russell-5'>, <User 'rydgel'>, <User 'petersonjackiem'>, <User 'mahmoud-kamal-10'>, <User 'meagan-ashley-1'>, <User 'morten-bagai'>, <User 'jeffmacintyre'>, <User 'jmcantrell'>, <User 'dj-lein'>, <User 'leah-culver'>, <User 'therationale'>, <User 'jplproduction'>, <User 'andrew-collie'>, <User 'robspectre'>, <User 'jmsdnns'>, <User 'goshakkk'>, <User 'rkonow'>, <User 'thomas-a-r-woelz'>, <User 'jerom-ray'>, <User 'derrick-mcneill'>, <User 'josh-huff-1'>, <User 'chryslynn-burkhart'>, <User 'josh-k'>, <User 'georgia-andrews-rossiter'>, <User 'schneems'>, <User 'jaely-louise-turner'>, <User 'textfiles'>, <User 'lakshman-prasad-1'>, <User 'fabiokung'>, <User 'snerangis'>, <User 'zain-memon'>, <User 'josh-fraser-4'>, <User 'sarah-berry-4'>, <User 'ltseeley'>, <User 'tswicegood'>, <User 'the_verge'>, <User 'broccolini'>, <User 'tenderlove-1'>, <User 'calebnei'>, <User 'robert-davis-22'>, <User 'createdestroyforget'>, <User 'sreejith-kesavan'>, <User 'bkmontgomery'>, <User 'julian255'>, <User 'yasunori-matsuki'>, <User 'robbyt'>, <User 'atmos-dot-org'>, <User 'bkeepers'>, <User 'bas-verkooijen'>, <User 'paparent'>, <User 'chris-jones-174'>, <User 'rebecca-goldman-1'>, <User 'paulosman'>, <User 'whitmo'>, <User 'thespinachincident'>, <User 'james-labove'>, <User 'jorilallo'>, <User 'jboxer'>, <User 'ajung-1'>, <User '7son75'>, <User 'vegasvalentine'>, <User 'steinhoefel1'>, <User 'entequak'>, <User 'm-todd'>, <User 'josh-crim'>, <User 'oboenerd'>, <User 'courtney-ryan-vance'>, <User 'michelle-greer'>, <User 'tracy-osborn'>, <User 'wayne-chang'>, <User 'gil-hildebrand'>, <User 'mth47'>, <User 'robert-petro'>, <User 'hero-jr'>, <User 'mvz'>, <User 'bleikamp'>, <User 'gulopine'>, <User 'zeeg99'>, <User 'saad-irfan'>, <User 'nathan-vencil'>, <User 'allyson-nichols'>, <User 'miksago'>, <User 'hilary-gerten'>, <User 'aryaevents'>, <User 'anatomyofashane'>, <User 'am2589'>, <User 'veritasbandminneapolis'>, <User 'skeevis'>, <User 'mrgandrews'>, <User 'alex-james-burns'>, <User 'uberjon'>, <User 'rudess'>, <User 'flemmingdoerken'>, <User 'robbyrussell'>, <User 'jamesproud'>, <User 'rob-martino'>, <User 'z-plan'>, <User 'teenageengineering'>, <User 'andrew-seeley'>, <User 'skrillex'>, <User 'ableton'>, <User 'childish-gambino'>, <User 'thebeatles'>, <User 'radiolab'>, <User 'zedd'>, <User 'watchingcars'>, <User 'jeremy-carbaugh'>, <User 'john-dorman'>, <User 'joshnesbitt'>, <User 'adamramadhan'>, <User 'helloitsliam'>, <User 'tmpvar'>, <User 'aviflax'>, <User 'ntlkt'>, <User 'maxfenton'>, <User 'brianmario'>, <User 'mintchaos'>, <User 'jaymichigan'>, <User 'shazow'>, <User 'sitwalkstand'>, <User 'moshgirl'>, <User 'myusuf3'>, <User 'bziade'>, <User 'shazow-1'>, <User 'spaaaaaaaaaaaaaaaaace'>, <User 'bj-rnsackemark'>, <User 'miss-bloody-mew'>, <User 'kevinjohnson-9'>, <User 'bfirsh'>, <User 'reedmunson'>, <User 'rezart'>, <User 'travismills'>, <User 'mattfallek'>, <User 'john-mangino'>, <User 'andrewmbaxley'>, <User 'phiiipdefranco'>]

    >>> len(kenneth.tracks)
    485

You'll note that these methods are slow, as we are paging down a real web browser to get this data.

But, it's available. Unlike their API.

*rimshot*.

