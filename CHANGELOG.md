# CHANGELOG


## v3.8.0
* issue #2377: Add Outbrain Smartfeed experiment
* issue #2382: Add verification to tmz-web deploy
* issue #2459: per-vendor consent escape hatch


## v3.6.1
* issue #2448: post-launch ketch adjustments


## v3.6.0
* issue #2431: ketch privacy updates


## v3.5.6
* issue #2426: set wbppid before requesting display ads


## v3.5.5
* Use correct composer version


## v3.5.4
* Use `triniti/core` v2.1.3


## v3.5.3
* [revert] issue #2386: Latest Recommendation to Fix Adhesion Banner


## v3.5.2
* Fix for "TV Shows" image sizes in watch section on tablet


## v3.5.1
* Fix to display slider widget images on tablet


## v3.5.0
* issue #2110: Add an explicit width and height to all images
* issue #2386: Latest Recommendation to Fix Adhesion Banner
* issue #2405: video ad_rule parameter is malformed


## v3.4.1
* issue #2390: hardening against invalid requests and responses


## v3.4.0
* issue #2390: hardening against invalid requests and responses


## v3.3.0
* issue #2322: Add trending bar to News, Sports, and Hip Hop home pages.
* issue #2336: remove blockthrough code
* issue #2341: IOS AppClip Integration For Web
* issue #2347: Gap Between Primary Video asset and Title on mobile web.
* issue #2363: Create ad-container for adhesion and header ads
* Health Check: added validation of essential resource loading
* Update docker base image for Sept 2022 to `wb/php8:0.6.0` (php 8.1.10-fpm-alpine3.16)
* Update composer to `composer:2.4.1`
* Update local redis to 6.2.7-alpine3.16
* Remove the ErrorsDashboard
* Update Dashboard to remove mon.sh
* Update CLOUD_INSTANCE_TYPE to prefix '${CPU_ARCH}-' vs 'fargate-'


## v3.2.0
* issue #2370: Transition video advertising config to JW dashboard


## v3.1.1
* issue #2364: Add Google Analytics 4 (GA4)


## v3.1.0
* issue #2105: Remediate event10 (Video Start) Adobe Analytics network call
* issue #2281: Watch Permalink Recommendations
* issue #2316: SEO Enhancements for Video URL & Sitemaps
* issue #2337: update video bidders
* issue #2344: add ad_rule query parameter to video ad tag url
* issue #2357: fix document blocks that dont render because they do not have an aspect ratio


## v3.0.1
* Fix SitemapController


## v3.0.0
__BREAKING CHANGES__

* Require `php>=8.1`.
* Use node v15.14.0.
* Use `gdbots/schemas` v3.0.1
* Use `triniti/schemas` v3.0.1
* Use npm gdbots/pbj 3.x.
* Use new php builtin enum instead of custom enum classes.
* Update docker base image for May 2022 to `wb/php8:0.5.0` (php 8.1.6-fpm-alpine3.15)
* Update composer to `composer:2.3.5`
* Allow Graviton Fargate
* Update CLOUD_INSTANCE_TYPE to prefix '${CPU_ARCH}-' vs 'fargate-'
* Slack Webhook URL moved to a variable
* Adjust wording of Slack deploy text
* __Modify Schemas:__
  * `gdbots:ncr:mixin:search-nodes-request` patch revision `1-0-4`
    * Add `track_total_hits` boolean field.
  * `gdbots:ncr:request:get-node-history-request` patch revision `1-0-1`
    * Add `topic` string field with pattern `^[\w\.-]+$`.
    * Add `partition` string field with pattern `^[\w\.-]+$`.
    * Add `sub_partition` string field with pattern `^[\w\.-]+$`.
  * `gdbots:pbjx:mixin:search-events-request` patch revision `1-0-1`
    * Add `track_total_hits` boolean field.


## v2.14.6
* issue #2293: hotfix for Adobe Analytics click tracking of "Do Not Sell" checkbox.


## v2.14.5
* Fix linting issue in analytics.js


## v2.14.4
* issue #2236: Allow robots to index Sports, Hip Hop, Watch and Photos after updating SEO html tags.
* issue #2259: SEO Updates for "Gallery"
* issue #2293: Ensure Adobe Analytics click tracking for the Opt Out is present on all "Do Not Sell" sections
* issue #2330: Browser notifications not firing


## v2.14.3
* issue #2215: Drop shadow for full width Primary assets should only be present on First article to separate from navbar
* issue #2230: Core Web Vital Optimizations
* issue #2272: Image Captions Shouldn't Be Full Width
* issue #2279: Quote Block issue
* issue #2288: Make JWPlayer "Live" Circle Red
* issue #2297: Remove bouncex script
* issue #2298: Remove Prism script
* issue #2299: Remove iris tv script


## v2.14.2
* issue #2271: Make All "Tabs" Across Mobile Web Evenly Spaced
* issue #2282: Remove clean.io script
* issue #2302: Upgrade SASS and remove dependency on Python 2
* issue #2307: power ads.txt and app-ads.txt from the cms


## v2.14.1
* issue #2107: Mobile and Tablet Only: When you select the navmenu header
(or options inside) sometimes focus remains on the blogroll
* issue #2216: See More" Adjustment & "Even More" Category Tag Cloud for Video Permalinks
* issue #2242: SEO Updates for "People" Pages
* issue #2243: SEO Updates for Video Permalinks
* issue #2260: Make "Thirty Mile Zone" in Desktop Footer an SVG instead of PNG.
* issue #2261: Add Hip Hop's Purple HEX Code to Style Guide.


## v2.14.0
* Implement fox strike ad library
* issue #2284: update app-ads.txt
* issue #2274: update ads.txt
* issue #2211: OneTrust Replacement


## v2.13.1
* Fix for video blocks, remove autoplay experiment


## v2.13.0
* issue #2246: Update "Read More Stories" & "Previous" link on Hip Hop
* issue #2017: Scroll Depth Tracking For Adobe Analytics.
* issue #2201: A/B Test For Browser Notifications Subscription Prompt
* issue #2244: fix safari header rendering bug when skin is present
* issue #2245: render in-between blogroll promotions for hip-hop


## v2.12.2
* issue #2251: Update app ads.txt


## v2.12.1
* hotfix zergnet widget for mobile articles


## v2.12.0
* issue #2198: Hip Hop Section


## v2.11.1
* Add site sub section to video permalink route in `WatchController`


## v2.11.0
* issue #2186: Watch TMZ Section


## v2.10.3
* issue #2184: hotfix for blogroll fragments


## v2.10.2
* Update docker base image for March 2022 to `wb/php8:0.4.0` (php 8.0.16-fpm-alpine3.15)
* Update composer to `composer:2.2.7`
* Increase LogGroup RetentionInDays to 365
* Fix mon.sh awk errors
* issue #2130: "Core Web Vitals" Measurement to only 5% of users.
* issue #2185: app_ads.txt update
* issue #2184: Adjust font sizing on smartphone so fragments break exactly the same as desktop
* issue #2223: Remove RN's applink config


## v2.10.1
* Fix issue with list gallery analytics


## v2.10.0
* Update docker base image for January 2022 to `wb/php8:0.3.0` (php 8.0.14-fpm-alpine3.15)
* Update composer to `composer:2.2.3`
* Update local redis to 6.2.6-alpine3.15
* issue #2137: nextup scrolling on smartphone
* issue #2146: Full Width Subassets on Mobile Web (fix)
* Fix bug in `youtube_video_block.twig` that was requesting an invalid image size


## v2.9.1
* issue #2179: undo temporary sfmc/privacy policy changes. (round 2)
* issue #2114: webpack hotfix for gallery release


## v2.9.0
* issue #2177: Update Browsi scripts for new AWS configuration.
* issue #2179: undo temporary sfmc/privacy policy changes.


## v2.8.4
* issue #2130: "Core Web Vitals" Measurement in Adobe Analytics


## v2.8.3
* issue #2114: List Gallery Enhancements
* issue #2130: "Core Web Vitals" Measurement in Adobe Analytics
* issue #2146: full width subassets on mobile web
* issue #2157: Full Width Primary Images on smartphone sports/news blogrolls.
* issue #2170: added new ads entry


## v2.8.2
* issue #2180: redirect /privacy and /terms to tmz pages


## v2.8.1
* issue #2138: use fox sfmc for newsletter flow (round 2)


## v2.8.0
* issue #2138: use fox sfmc for newsletter flow


## v2.7.5
* issue #2166: privacy redirects (round 2)


## v2.7.4
* issue #2166: privacy redirects


## v2.7.3
* use `new Response()` instead of `Response::create()`


## v2.7.2
* issue #2144: Removed duplicate h1 tags for SEO optimization
* issue #2145: fix share icon styling and query parameters.
* issue #2148: Update app-ads.txt for maz
* Set X_FORWARDED_PORT as string instead of int
* Use `tmz/core` v2.1.4
* Use `symfony/http-kernel` v5.4.0
* Use `symfony/security-bundle` v5.4.0


## v2.7.1
* Fix page.js linting issue.


## v2.7.0
* issue #2082: A/B Experiment to assess Autoplay performance
* issue #2102: update app-ads.txt
* issue #2103: add synacor to jwplayer bidders
* issue #2108: Update ads.txt for wunderkind.
* issue #2116: Remove picture in picture button from JW Player
* issue #2118: smartphone share buttons - adjust style and add query parameter to url
* issue #2131: Prevent non-lightbox galleries from preloading gallery component.


## v2.6.2
* issue #2127: Fix gallery promotions and templates.


## v2.6.1
* Update docker base image for October 2021 to `wb/php8:0.2.2` (php 8.0.11-fpm-alpine3.14)
* Update composer to `composer:2.1.9`
* Update local redis to 6.2.6-alpine3.14
* Updated TMZ dev email.


## v2.6.0
* Initial transfer to TMZ/Fox.


## v2.5.1
* Fix gallery block launch text.


## v2.5.0
* issue #2027: List Gallery Layout on TMZ.
* issue #2049: non-homepage alert widget + ad styling issues
* issue #2082: A/B Experiment to assess Autoplay performance
* issue #2083: Infinite scroll promotion slot loading stops working on sports once the next page loads
* issue #2086: update app-ads.txt
* issue #2094: Add Native App Links to Mobile Menu


## v2.4.0
* issue #2019: Remove 'theme' 'channel' & 'hashtags' from cust_params in ad calls
* issue #2038: Smartphone Web: Super Heroed Article Headline Fragments Should Respect Gutters So They Have The Same Line Break As Article Pages.
* issue #2043: update smartphone lightbox container height to 100% to contain tall images
* issue #2047: Make "Related Articles" live for 100% of of Smartphone HP visitors on prod
* issue #2050: Smartphone Only: Hyper link text in lists is not showing up red
* issue #2060: update `ads.txt.twig`
* issue #2069: update style guide font download links
* issue #2074: update zergnet widgets
* issue #2077: Remove Promos at the End of Sports Articles


## v2.3.0
* Update docker base image for July 2021 to `wb/php8:0.2.0` (php 8.0.8-fpm-alpine3.14)
* Update composer to `composer:2.1.3`
* Update local redis to 6.2.4-alpine3.14
* Update docker-compose.yaml to version 3.8
* Fix "Expecting value" error in mon.sh.
* Fix apache/fpm memory graphs in CloudWatch Dashboard.
* Add qa.sh script for QA Automated testing


## v2.2.2
* issue #2045: update `ads.txt.twig`
* issue #2053: update `app_ads.txt.twig`


## v2.2.1
* Fix `ShowController` `NodeRef` use statement.


## v2.2.0
* issue #1956: tmz-web :: Newsletter promo


## v2.1.2
* hotfix issue #2014 - adjust sizing and placement of tmz shop logo in permalink blogroll


## v2.1.1
* hotfix issue #2014 - styling for StackCommerce Ad unit


## v2.1.0
* issue #2014: Migrate Remaining StackCommerce Ad units to TMZ Widgets
* issue #2016: Click Tracking For Polls
* Fix search render when there is no q string.


## v2.0.3
* Fix `SitemapController`.


## v2.0.2
* Update docker base image for June 2021 to `wb/php8:0.1.3` (php 8.0.6-fpm-alpine3.13)
* Update composer to `composer:2.0.14`
* Update local redis to 6.2.3-alpine3.13
* Prefer `docker compose` over `docker-compose`
* Implement DeploymentCircuitBreaker
* Use `tmz/core-php` v2.0.4.


## v2.0.1
* Add ElasticSearch timeouts.
* Scaling config.


## v2.0.0
* Symfony 5 updates.
* Use `tmz/core-php` v2.0.0.


## v1.36.1
* issue #2029: Re-introduce "Tours" Nav Item


## v1.36.0
* issue #1968: Smartphone Only: Cannot zoom in on galleries images.
* issue #2003: Img blocks are missing alt attribute description
* issue #2013: Security :: Update jQuery library from 2.2.4.


## v1.35.2
* issue #1955: Related article experiment hotfix
* issue #1973: Exit link tracking happening on certain articles
* issue #2005: Fix styling of media video swipes
* issue #2006: Fix headers on show listings page mobile.


## v1.35.1
* issue #1965: Optimize Jw-Player script
* Fix breaking header text, mobile headers, and punctuation on listings page.


## v1.35.0
* issue #1946: Adjustment of TMZ Shop Units
* issue #1955: Related Articles Experiment
* issue #1979: Unable to swipe Up Next galleries
* issue #1982: Update Desktop/Tablet Show Listings Page
* issue #1989: When requesting mobile website image magnifying icon is misplaced and crashes site when clicked on.
* issue #1999: Headline linebreaks on blogroll stories should match linebreaks of their corresponding article permalinks
* Load prism js on all pages, with consent check.


## v1.34.0
* Update docker base image for April 2021 to `wb/php:0.10.1` (php 7.4.16-alpine3.13)
* Update local redis to 6.2.1-alpine3.13
* Remove AnomalyDetector alarms


## v1.33.6
* Reduce dropshadow from top of homepage blogroll
* Remove media swipes from content blocks and into article and blogroll templates


## v1.33.5
* issue #1892: Migrating hotjar to web off of GTM.
* issue #1895: iOS - Safari - Web: Video assets will start playing with CC on without captions, requiring users to toggle off/on for CC.
* issue #1945: Adjusted displayed dates for tmz-on-tv and tmz-live shows pages.
* issue #1947: Shows Section, use episode title instead of 'Latest Episode'
* issue #1954: Move article swipe out of first block and into title region
* issue #1961: Adjust Smartphone Web Non-Sports Swipes to have White Lettering.
* issue #1969: Smartphone : Add Drop Shadow effect and Remove Padding from Homepage Blogroll Full width Primary.
* issue #1972: IOS - Banner recommending to download TMZ App is not dismissible
* Smartphone Web: Adjust first story in blogroll to have full width primary art when classification is set to `super-hero`.


## v1.33.4
* hotfix - adding swipe to primary images from blogroll.
* hotfix - fixing safari swipe position issue.


## v1.33.3
* issue #1714: Attempt to fix css build issues.
* hotfix - issue #1922: Remove slider horizontal scrollbar.


## v1.33.2
* issue #1714: Image lightbox css adjustment
* issue #1922: Smartphone Web: Slider Widget Design Update.


## v1.33.1
* issue #1714: Image lightbox bug fix
* issue #1936: Smartphone Web: align header title on search results page hotfix


## v1.33.0
* issue #1714: Image lightbox
* issue #1920: Smartphone Web: Blogroll Header Design Adjustment
* issue #1921: Smartphone Web: New Most Popular Unit
* issue #1924: Smartphone Web: Adjust first story in homepage blogroll to have full width Primary Art.
* issue #1936: Smartphone Web: align header title on search results page


## v1.32.0
* Update docker base image for March 2021 to `wb/php:0.10.0` (php 7.4.15-alpine3.13)
* Update composer to `composer:2.0.11`
* Update local redis to 6.0.12-alpine3.13
* Hide PHP X-Powered-By header


## v1.31.0
* issue #1791: TMZ Gallery Design Updates (Smartphone ONLY)
* issue #1873: Gallery Blocks- Start at poster image sequencing broken.
* issue #1879: Remove System1 From Search Pages
* issue #1916: Hide Spinner on video play.
* issue #1923: Smartphone Web: Darken The TooFab Promo Unit.
* issue #1925: smartphone: after closing an article's lightbox gallery after having loaded a new gallery from the end card, take the user back to the article
* issue #1931: Smartphone - Noticed That The Bottom Extra Content "Latest Galleries" Will Be Repainted When Toggling Between Detailed And Non-Detailed View
* Adds TMZ RN Application to `apple_app_site_association` for Deep Linking on iOS.


## v1.30.1
* issue #1872: Autoplay on Video.
* issue #1884: Lightbox Galleries are sometimes stalling on images, not allowing user to go to next or previous.
* issue #1899: Add "Careers" link to Mobile Web Nav
* issue #1906: ad skin shows white rectangle when in-site alert is present
* issue #1908: Update `ads.txt` with latest file (2021-02-10) from adops.


## v1.30.0
* Upgrade to REDIS_V60_SHARED_ENDPOINT.
* Use `tmz/core` v1.13.0


## v1.29.1
* issue #1878: Update `ads.txt` with latest file (2021-01-19) from adops.
* issue #1888: remove tmz sports tab from shows pages
* issue #1890: Update Careers Link
* Update `app_ads.txt` with latest file (2021-01-19) from adops.
* Update `release.md` template
* Onetrust thirdparty changes


## v1.29.0
* Update docker base image for January 2021 (php 7.4.14) from `wb/php:0.9.4` to `wb/php:0.9.5`
* Update composer from `composer:2.0.4` to `composer:2.0.8`
* Update local redis to 6.0.10


## v1.28.1
* issue #1749: implement jwplayer tooltip thumbnail sprite/track
* issue #1845: video preroll can cover smartphone menu
* issue #1851: Document Blocks with Launch are defaulting to 4 by 3 when set to other aspect ratios and Document Blocks without launch text are using full Poster image size.
* issue #1862: Smartphone Web: Sports PAGE IS NOT ENDLESS.
* issue #1863: Video controls should not be visible on initial video play - smartphone only


## v1.28.0
* issue #1605: Mobile web video controls should not be visible until user taps on video
* issue #1701: Jwplayer custom float implementation.
* issue #1803: Lightbox analytics updates.
* issue #1843: Smartphone web Sports tab endless blogroll is broken
* issue #1844: Update `ads.txt` with latest file (2020-12-14) from adops.
* issue #1848: Remove "Shop" from Smartphone Top-of-Page Nav Menu
* issue #1853: remove telaria from jwplayer bidder config
* issue #1857: Onetrust v2 implementation
* issue #1858: Update `app_ads.txt` with latest file (2020-12-23) from adops.
* update `release.md` template


## v1.27.0
* issue #1354: Iris.TV Contextual Targeting
* issue #1733: Desktop/Safari -- Clicking next photo gets hung up and also lags
* issue #1768: Remove skip back 10 seconds and pause/play buttons on Tablet.
* issue #1771: Add Shop Section
* issue #1811: overflow css fix for ad in article permalink blogroll widget
* issue #1825: Update facebook-video-block set max-width to 500px and overflow hidden.
* issue #1826: Update `ads.txt` with latest file (2020-11-30) from adops.
* issue #1835: remove browsi viewability experiment code
* issue #1840: Ad "adid" to all ad requests (display and video).
* Use `updated_at` to determine cache time instead of `published_at` in `AbstractController::deriveMaxAgeFromFreshness`.


## v1.26.0
* issue #1651: Add System1 search ads
* issue #1816: Facebook share icon is missing on mobile IOS devices
* Add http security headers
* Update docker base image for November 2020 (php 7.4.12) from `wb/php:0.9.3` to `wb/php:0.9.4`
* Update composer from `composer:1.10.13` to `composer:2.0.4`
* Update local redis to 5.0.10
* issue #1563: Implement Ad Frequency Capping
* issue #1793: Remove disqus code from tmz-web
* issue #1802: Fix smartphone "start-at-poster" feature.
* issue #1817: TMZ - Update .updated styling for Article-block and Browsi Ad, Set article font-size to 18px desktop, 19px smartphone


## v1.25.2
* issue #1796: Increase font size by 25% on Smartphones.
* issue #1806: Update smartphone header sizes.


## v1.25.1
* issue #1712: Browsi Ad Viewability Experiment.
* issue #1787: Update `ads.txt` with latest file (2020-10-23) from adops.


## v1.25.0
* issue #1601: Create Styleguide Entries for Native Ad Units.
* issue #1707: Update Prebid to v4.10.0
* issue #1774: Add media credit below video for video-block, playlist widget and video permalink on smartphone.


## v1.24.2
* issue #1496: Hotfix for hiding in-site alert when clicking the alert link.
* issue #1690: Hotfix for smooth scrolling.
* issue #1701: Hotfix to remove Jwplayer custom float implementation.
* Update docker base image for October 2020 (php 7.4.11) from `wb/php:0.9.2` to `wb/php:0.9.3`
* Update composer from `composer:1.10.12` to `composer:1.10.13`


## v1.24.1
* issue #1690: clicking on float player should result in auto scroll to primary player
* issue #1701: Jwplayer custom float implementation.
* issue #1753: CC Option not working as intended on Web.
* issue #1763: Update block fix for Browsi Ads.
* issue #1772: Update `app_ads.txt` with latest file (2020-10-09) from adops.
* Use `tmz/core` v1.11.2


## v1.24.0
* issue #1496: In-Site Alerts on Web
* issue #1674: Removing jwplayer/kaltura flags and chunks of kaltura code.
* issue #1704: Disable up next/recommendations videos when "show related videos" is false.
* issue #1739: Adjust TMZ Sports on FS1 Show Section to point to the TMZ Sports on FS1 YouTube Playlist.
* issue #1747: Update `ads.txt` with latest file (2020-09-14) from adops.
* Update docker base image for September 2020 (php 7.4.10) from `wb/php:0.9.1` to `wb/php:0.9.2`
* Update composer from `composer:1.10.9` to `composer:1.10.12`


## v1.23.1
* hotfix - issue #1154: Jwplayer Recommendation Regex Fix For Safari Browsers


## v1.23.0
* issue #1154: JWPlayer Recommendations
* issue #1726: Update `ads.txt` with latest file (2020-08-18) from adops.
* issue #1728: caption styling issues
* issue #1735: Update `ads.txt` with latest file (2020-09-02) from adops.
* Fix ScalingPolicy CloudWatch Alarms
* Use `triniti/schemas` v1.1.12
* Use `tmz/schemas` v1.1.11
* Use `tmz/core` v1.11.1


## v1.22.1
* issue #1721: Update `ads.txt` with latest file (2020-08-04) from adops.


## v1.22.0
* issue #1710: Update `app_ads.txt` with latest file (2020-08-05) from adops.
* Update docker base image for August 2020 (php 7.4.8) from `wb/php:0.9.0` to `wb/php:0.9.1`
* Update composer from `composer:1.10.8` to `composer:1.10.9`
* Updated the ECS Service PlatformVersion from 1.3.0 to 1.4.0
* Use `gdbots/ncr` v1.0.15
* Use `gdbots/schemas` v1.6.6
* Use `tmz/core` v1.10.2
* Use `tmz/schemas` v1.1.10
* Use `triniti/dam` v1.0.7
* Use `triniti/ovp` v1.3.3
* Use `triniti/apple-news` v1.1.2
* Use `triniti/apollo` v1.0.1


## v1.21.1
* issue #1685: Videos Page: One Unscheduled Video Will Not Let Users Select Other Videos
* issue #1705: allow logged in users to view unpublished video permalinks


## v1.21.0
* issue #1413: add extra content gallery lightbox smartphone
* issue #1577: Gallery Lightbox Ads not refreshing when user cycles through images
* issue #1671: Update `ads.txt` with latest file (2020-07-14) from adops.
* issue #1691: add video title on hover when up next video plays.
* Add StackCommerce to wbconsent vendors list.
* Update docker base image for July 2020 (php 7.4.7) from `wb/php:0.8.1` to `wb/php:0.9.0`
* Update composer from `composer:1.10.07` to `composer:1.10.8`
* Update alpine-linux from v3.11 to v3.12


## v1.20.2
* hotfix - issue #1680: Update scrubber knob selection
* hotfix - issue #1681: Update floating video close button to have a larger hit area
* hotfix - issue #1682: Update share modal title to uppercase


## v1.20.1
* hotfix - incorrect tagging for v1.20.0


## v1.20.0
* hotfix #1495: JWPlayer Front End


## v1.19.4
* issue #1663: Bring back tmz-on-tv shows (again) Round 2


## v1.19.3
* issue #1663: Bring back tmz-on-tv shows (again)


## v1.19.2
* issue #1660: Remove tmz-on-tv shows (again) (also remove tours without needing css hack)


## v1.19.1
* issue #1652: Bring back tmz-on-tv shows
* issue #1649: Update `ads.txt` with latest file (2020-07-02) from adops.


## v1.19.0
* Update `ads.txt` with latest file (2020-06-18) from adops.
* issue #1576: Update ads.txt with latest file (2020-05-26) from adops.
* Update docker base image for June 2020 (php 7.4.6) from `wb/php:0.7.0` to `wb/php:0.8.1`
* Update composer from `composer:1.10.0` to `composer:1.10.7`
* Update local redis to 5.0.9
* Switch back to httpd.conf from base image
* Adjusted LogGroup `RetentionInDays` from 7 to 30
* Add build rejection steps to the release template.
* issue #1638: finalize shows changes


## v1.18.14
* issue #1642: end card videos do not have their own end card


## v1.18.13
* hotfix for video end card not firing kBind secondQuartile.


## v1.18.12
* issue #1624: Prevent `tmz-on-tv` shows. (refine routing and redirects)


## v1.18.11
* issue #1624: Prevent `tmz-on-tv` shows.
* 302 redirect `/shows/tmz-on-tv/` to `/shows/`.
* Remove 302 redirects for `/shows/tmz-live`, `/shows/tmz-sports/`, and `/shows/tmz-newsroom/`.


## v1.18.10
* issue #1621: Prevent `tmz-on-tv` video content from being accessed via permalink or search request.


## v1.18.9
* 302 shows pages to home route.


## v1.18.8
* issue #1570: Adjust Browser Notifications to override the previous notification, so they don't stack.
* issue #1588: Add Connatix "Hot Video" Unit to Mobile Web


## v1.18.7
* Hotfix for util selecting a null noderef.


## v1.18.6
* Version number issue.


## v1.18.5
* Removing `--storage-driver=overlay` to fix docker build issue.


## v1.18.4
* issue #1556: Adding browsi flag check


## v1.18.3
* issue #1556: Browsi in content ads


## v1.18.2
* make apple app association inert


## v1.18.1 [REVERTED]
* issue #1556: Browsi in content ads


## v1.18.0 [REVERTED]
* Update docker base image for May 2020 (php 7.4.5) from `wb/php:0.7.0` to `wb/php:0.8.0`
* Update local redis to 5.0.9
* Switch back to httpd.conf from base image
* Update `ads.txt` with latest file (2020-05-05) from adops.
* Add fluid to smartphone medium_rectangle adSize in `renderAdsFlow.js`.
* Add flag for `gpt_collapse_empty_divs_enabled` (defaults to false) in `renderAdsFlow.js` so we can turn that on if needed.


## v1.17.2
* issue #1537: Adjust Sports to Run Off Of Category Instead Of Channel -- fix the /featured/sports/ invalid ref.


## v1.17.1
* issue #1413: Fixed missing context check in lightboxer.js line: 51.
* issue #1537: Adjust Sports to Run Off Of Category Instead Of Channel -- don't show sports theme banner on the tmzsports category either.


## v1.17.0
* issue #1413: Expanding the Lightbox Galleries to include more content and ads on desktop
* issue #1537: Adjust Sports to Run Off Of Category Instead Of Channel
* issue #1548: Smartphone permalink style updates
* issue #1553: Implement StackCommerce Tracking Pixel
* Update `ads.txt` with latest file (2020-04-22) from adops.
* Update `app_ads.txt` with latest file (2020-04-17) from adops.


## v1.16.0
* Use `tmz/core` v1.7.8
* issue #1523: Make video playlist disabled until pre-roll finishes
* issue #1304: Standardize all blocks round 2
* issue #1481: Desktop only: If an article has no asset blocks it won't hoist the primary image in the blog roll
* issue #1536: Remove bluekai
* issue #1538: Update nav-desktop__item--showtimes link color
* Update `ads.txt` with latest file (2020-04-09) from adops.
* Upgrade prebid from `v3.13.0` to `v3.15.0`
* issue #1548: Update smartphone permalink styles, #ad-permalink1 margins and blogroll img embed-responsive ratio


## v1.15.0
* issue #1304: Standardize all blocks
* issue #1525: Add Synacor Media to bidders and gracefully upgrade Prebid JS from `v2.39.0` to the `v3.13.0`
* Update `ads.txt` with latest file (2020-03-31) from adops.
* Update `app_ads.txt` with latest file (2020-03-26) from adops.
* Update awscli to 1.18.x to allow for `aws ecr get-login-password`
* Update docker base image for March 2020 (php 7.4.3) from `wb/php:0.6.0` to `wb/php:0.7.0`
* Update local redis to 5.0.8
* Add lightbox as allowed section for promotion and widget controller endpoints.
* Permanently redirect `/categories/r-i-p.*` requests to `/categories/rip/`. ref https://github.com/wb-apps/tmz-api/issues/516
* Use `gdbots/schemas` v1.6.5
* Use `tmz/core` v1.7.6
* Use `tmz/schemas` v1.1.7
* Use `triniti/schemas` v1.1.8


## v1.14.1
* Use `tmz/core` v1.7.4 with:
  * Fix bug with FpcEdgeWriter to ensure all headers are strings so AWS cloudfront/edge don't error out.
  * Do not include `swipe` field in Elasticsearch `_all` field.
  * Change `FpcEdgeWriter::shouldWrite` to allow for 1-100% for writes and when it's a very short s-maxage, use 51-100% (to reduce cost).
* issue #1275: Add image-block toofab theme support for no link layout


## v1.14.0
* Catch errors from client side fetch using `response.ok` check so no server errors get rendered for async requests.
* issue #1275: Implement "toofab" theme for image block for both aside:true or false conditions.
* issue #1404: TMZ Accessibility - Skip Link
* issue #1406: TMZ Accessibility - Keyboard Tab Focus and Order
* issue #1407: TMZ Accessibility - Alt text for all images and links
* issue #1408: TMZ Accessibility - Nested Heading for Articles
* issue #1409: TMZ Accessibility - Form Field Label
* issue #1417: TMZ Accessibility - Keyboard Tab Focus and Order - Photo Gallery modal
* issue #1423: TMZ Accessibility - Keyboard Tab Focus and Order - Tab Focus Styling
* issue #1445: TMZ Accessibility - Sports Section Page accessibilities
* issue #1447: TMZ Accessibility - Photos Section Page accessibilities
* issue #1448: TMZ Accessibility - Video Section Page accessibilities
* issue #1449: TMZ Accessibility - Category Page
* issue #1450: TMZ Accessibility - People Page
* issue #1453: TMZ Accessibility - TMZ Live Page accessibilities
* issue #1454: TMZ Accessibility - TMZ on TV Page accessibilities
* issue #1466: TMZ Accessibility - Home page - Smartphone
* issue #1469: TMZ Accessibility - Modal/Lightbox Screenreader focus trap
* issue #1472: TMZ Accessibility - Videos Page - Smartphone
* issue #1473: TMZ Accessibility - Photos Page - Smartphone
* issue #1474: Fixing `undefined` on gallery arrow click analytics.
* issue #1475: TMZ Accessibility - TMZ on TV & TMZ Live - Smartphone
* issue #1476: TMZ Accessibility - Article page - Smartphone
* issue #1477: TMZ Accessibility - People, Category, Search Result Pages - Smartphone
* issue #1493: Multiple notifications are sent when the site is running on multiple browser windows.
* issue #1504: Apple-app-site-association.txt needs to be added Server side.
* issue #1508: remove text (NEW) from privacy policy in footer


## v1.13.1
* issue #1488: update the unblock notifications instruction for Microsoft Edge browser.
* Update `ads.txt` with latest file (2020-02-21) from adops.
* Include `x-node-updated-at` and `x-node-ref` headers in permalink responses.
* Use `tmz/core` v1.7.1 with `FpcEdgeWriter` that uses `x-node-updated-at` header to inform edge writes.


## v1.13.0
* issue #1264: Click Tracking for links in articles.
* issue #1342: Browser Notification Enhancements
* issue #1480: Make browser notifications persistent.
* Use `tmz/core` v1.7.0 with `FpcEdgeWriter` percentage strategy.


## v1.12.2
* Use `tmz/core` v1.6.6 with `FpcEdgeWriter` fix for missing symfony `_route` attribute.


## v1.12.1
* Use `tmz/core` v1.6.5 with aws credential and fpc edge throttle cache in redis instead of apcu/opcache in attempt to eliminate the cache slam.


## v1.12.0
* issue #1248: Add Livestream Schema to web when video is live within article, shows page or on video permalink
* issue #1342: Browser Notification Enhancements
* issue #1428: Make read-more permanent
* issue #1457: Remove Vilynx from EVERYTHING
* Use `tmz/core` v1.6.4 with FpcEdgeWriter modulyolo.


## v1.11.0
* Use new `gdbots/ncr-bundle` with ssl config for elastica client which hopefully improves performance by using http2 for search requests.
* Add `php /app/bin/console app:compile-twig-templates --no-interaction --no-debug > /dev/null` to entrypoint to eliminate opcache thundering herd issue.
* Use `tmz/core` v1.6.3 with FpcEdgeWriter throttling back-off.


## v1.10.3
* Use `tmz/core` v1.6.2 with FpcEdgeWriter changes to store item in cache for 7 days.


## v1.10.2
* DO NOT DEPLOY to prod - FpcEdge and load testing tweaks.
* Add `Cache-Control "max-age=86400, public"` to all static files that apache serves.
* Ignore google robots from voting in `PollController::vote`, srsly google honor the _ing robots exclusion.


## v1.10.1
* Use `tmz/core` v1.6.1 with FpcEdgeWriter tweaks to ensure we don't cache empty responses.


## v1.10.0
* Use `tmz/core` v1.6.0 with new FpcEdgeWriter, this writes to dynamodb on all fpc misses.  Service can be disabled with flag `fpc_edge_writer_disabled`.
* Add debugging endpoints for opcache (`/_/xopcache/`) and apcu (`/_/xapcu/`).  These require `xdebug_enabled` flag to be on.
* Add back `<Proxy>` to vhost so we can increase the apache proxy timeout.  This is primarily for localhost since request take much longer.


## v1.9.3
* Use `tmz/core` v1.5.3 with redis cluster timeout adjustments.


## v1.9.2
* More Redis cluster tweaks and optimizations.
* Apache and FPM optimizations and changes for stabilization. (mpm_event instead of mpm_prefork and fpm children from 200 to 20).
* Set reasonable timeouts:
  * elasticsearch connection timeout from 30 to 2 seconds
  * redis from basically unlimited to 0.2 seconds with 3 max reconnect attempts


## v1.9.1
* Use `tmz/core` v1.5.1 with new redis cluster proxy and adapter support.
* Update `ads.txt` with latest file (2020-01-30) from adops.


## v1.9.0
* WARNING!! Use `tmz/core` v1.5.0 with new redis proxy and adapter, need to load test this before production.


## v1.8.0
* Use new schemas with optimized (de)serialize for identifier objects.
* WARNING!! Use `tmz/core` v1.4.0 with new redis namespace, all apps must roll out around the same time.
* Remove `APP_REDIS_PERSISTENT_ID` and `FPC_REDIS_PERSISTENT_ID` from environment config since `tmz/core` does it now.
* Use `gdbots/schemas` v1.6.4
* Use `tmz/schemas` v1.1.6
* Use `triniti/schemas` v1.1.7


## v1.7.1
* Set the `APP_REDIS_PERSISTENT_ID` and `FPC_REDIS_PERSISTENT_ID` to share the same value to reduce the total volume or persistent connections by half.


## v1.7.0
* issue #492: SameSite Cookie Policy Updates
* issue #1357: Make widget configuration on "sports" articles the same strategy for all device views.
* issue #1343: Add unique page name for infinite scrolling pages
* Update docker base image for January 2020 (php 7.4.1) from `wb/php:0.5.1` to `wb/php:0.6.0`
* Update `ads.txt` with latest file (2020-01-17) from adops.
* Update `app_ads.txt` with latest file (2020-01-22) from adops.
* Add new endpoints for widgets (e.g. `/_/gridler-widget/{id}/main.html`) so we can render them by id without promotion slots (for adhoc use like TMZ Talent page).
* Use `tmz/schemas` v1.1.5
* Use `triniti/schemas` v1.1.6


## v1.6.6
* Add more protection against onetrust running without all expected "always active" groups.
* issue #1401: video events firing wrong prop/evar values when there is a comma in the title.


## v1.6.5
* issue #1393: Homepage: When user clicks next to view 2nd, 3rd, nth page of blogs, it skips 1 article.
* Allow Smartnews, User-agent: Crowsnest, to robots.txt for dev environment.


## v1.6.4
* The Grapes of CCPA Wrath :: I Onetrusted you, again.


## v1.6.3
* The Grapes of CCPA Wrath :: Even the comscore, a kaltura original.


## v1.6.2
* The Grapes of CCPA Wrath, Part 3.


## v1.6.1
* The Grapes of CCPA Wrath, Part 2.


## v1.6.0
* The Grapes of CCPA Wrath.
* Use `tmz/schemas` v1.1.4
* Use `triniti/schemas` v1.1.5


## v1.5.2
* issue #1306: Modify ComScore Scorecard Research Tag for /featured/sports.
* issue #1386: Apply read more button styling (like homepage) to Sports, Channel and Category pages
* Removed hyphens auto from news.
* Update `ads.txt` with latest file (2019-12-12) from adops.
* Update `app_ads.txt` with latest file (2019-12-19) from adops.


## v1.5.1
* issue #1360: Change adRefresher to dispatch renderAds instead of direct GPT refresh.
* issue #1380: Add js-track-link to blogroll widget page button and ensure data-context is on page break block link


## v1.5.0
* issue #1249: Back/Forward button positioning precision improvements.
* issue #1286: Unify analytics project.
* issue #1295: Replacing VWO inline JS code with script reference.
* issue #1341: Fix gumgum bidder cfg function to really really get `inScreen` correct this time.
* issue #1350: Use show permalink link for live videos where show is populated
* issue #1369: Use pagination for blogroll widgets (when in main).
* Update `ads.txt` with latest file (2019-11-26) from adops.


## v1.4.6
* issue #1295: Updating VWO script and skipping DataLayer calls if vwo will redirect.
* issue #1341: Add gumgum bidder to prebid with `inScreen` instead of `isScreen`.
* issue #1351: Adjust Video Caption Styling To Have Black Background
* Update `ads.txt` with latest file (2019-11-18) from adops.
* Update `deploy.sh` script to be aware of branch deployments


## v1.4.5
* issue #1288: Adjust Watch TMZ page to play TMZ Rap Promo on Weekends
* issue #1296: Adjust blogroll sponsor styles for desktop
* issue #1317: Safeframe set to slot-specific not page
* issue #1335: Implement divider block on print - fix the "print" platform template to extend correct base block.
* issue #1341: Add gumgum bidder to prebid (and teads, telaria though not used yet.).  prebid is also upgraded from v2.17.0 to v2.39.0.
* issue #1347: In blocks, use "o" image version when can_use_launch_text is false
* Upgrade docker base image from `wb/php:0.5.0` to `wb/php:0.5.1` & composer to 1.9.1


## v1.4.4
* issue #1274: Implement divider block
* issue #1276: Updating player omniture configs to send tmz-web as app name, device view. Removing prop/evar 11 && 12. Removed stage environment.
* issue #1308: list link needs to be red/ bold
* issue #1316: update newsletter email validation to use isValidEmail.js
* issue #1325: Remove fadeout effect for page-break-blocks.
* issue #1326: Do not remove social buttons and related articles in blogroll widget when article has no page break
* issue #1335: Implement divider block on print (and feeds)
* Add `missing_block` and `missing_widget` templates to apps that are missing them.
* Update `ads.txt` with latest file (2019-10-28) from adops.
* use `tmz/core` v1.2.20
* use `triniti/canvas` v1.0.1, a new twig function `canvas_has_block` has been added to `CanvasExtension`.


## v1.4.3
* issue #1321: Make read more experiment variant on by default.


## v1.4.2
* issue #1312: Prevent skin ads from re-rendering.
* issue #1314: Add rubicon bidder param position to `renderAdsFlow.js`.
* Do not submit token if falsey in `subscribeToBrowser.js`.


## v1.4.1
* issue #1074: Change newsletter button color and hover.


## v1.4.0
* issue #1074: Create a Newsletter Form Page
* issue #1193: Display browser notifications to the user.
* issue #1299: Remove Podcast Section and all pages.
* issue #1300: Enable SafeFrame for googletag, e.g. `googletag.pubads().setForceSafeFrame(true)` if flag `safe_frame_enabled` is true.
* Upgrade docker base image (201908) from `wb/php:0.4.1` to `wb/php:0.5.0`
* Remove `beberlei/assert` constraint from composer now that php-intl extension is installed.
* Add `metas` to all envelopes returned with benchmark, timestamp, timestamp_iso for debugging.
* Update `ads.txt` with latest file (2019-10-16) from adops.
* Update `app_ads.txt` with latest file (2019-10-08) from adops.
* Update privacy policy and ad choices links per WB Legal.
* Use `tmz/core` v1.2.19
* Use `tmz/schemas` v1.1.0
* Use `triniti/notify` v1.0.8
* Use `triniti/schemas` v1.1.0


## v1.3.7
* issue #1252: Update tmz web app Dashboard to use Container Insights
* issue #1212: Revert autoplay videos on video permalink page in smartphone view (selector.js as well)


## v1.3.6
* Update `app_ads.txt` with latest file (2019-10-01) from adops.
* issue #1212: Revert autoplay videos on video permalink page in smartphone view.


## v1.3.5
* issue #1078: Add Clean.io Script to Page for Anti-Malvertising Trial. Added to `base.html.twig` before gpt with defer and guarded by flag `cleancreative_enabled` which defaults to true.
* issue #1245: Move Blockthrough's `window.BT.clearThrough` function in `renderAdsFlow.js` to after all logic about if ads should render at all.
* Update `ads.txt` with latest file (2019-09-27) from adops.
* Autoplay videos on video permalink page in smartphone view.


## v1.3.4
* issue #1212: Mobile web video captions.
* issue #1245: Add Blockthrough's updated Clearthrough function to `renderAdsFlow.js`.
* issue #1266: Add nl2br filter to `spotlight-widget` description field.
* Use `tmz/core` v1.2.12
* Use `tmz/schemas` v1.0.6
* Use `triniti/schemas` v1.0.7


## v1.3.3
* issue #1233: Pass from_refresh slot level targeting
* issue #1244: In `renderAdsFlow.js` modify expected sizes for Billboard, Billboard Flex, Leaderboard and Leaderboard Flex
* issue #1253: New "toofab-large" theme for spotlight-widget
* issue #1254: Adjust Anchor In Read More To Land On Block That Is Faded Out Instead Of Block After
* Update `ads.txt` and `app_ads.txt` with latest files (2019-09-18) from adops.
* Use `tmz/core` v1.2.11


## v1.3.2
* issue #1243: Add `display` property to `continued-anchor` CSS class to fix page scrolling position in Safari


## v1.3.1
* issue #1243: "Read More" button links user to `page-break-block` position on subsequent page


## v1.3.0
* issue #1138: Lazy Load Images
* issue #1218: Adding poster image to youtube block will resize the video player
* issue #1225: added `start_at_poster` option on gallery block.
* issue #1235: Update `app-ads.txt`
* issue #1237: Update `ads.txt`
* Remove `amp_video_enabled` flag check on video permalink.
* In `renderAdsFlow.js` default `ad_refresher_enabled` flag check to true.
* In `renderAdsFlow.js` change 33across bidder config to require `siteId` since although the doc says it's a publisher Id which is almost universally a global value, in 33across it's a per slot value.
* Use `triniti/dam` v1.0.2


## v1.2.0
* issue #1073: Ad Blocking Recovery
* issue #1148: Enabled ad refresh.
* issue #1174: Add Pubmatic to Header Bidding - use new publisherId.
* issue #1194: add amphtml reference to video permalink. (requires amp.tmz.com video permalink to be live first!)
* issue #1207: Update App-ads.txt
* issue #1210: Update ads.txt
* issue #1211: Force the `vwo_variant` value in `cust_param` key to persist throughout the user session using a cookie.
* require a specific package version for `beberlei/assert`, until we get the docker image updated with all the required extensions turned on
* Use `gdbots/schemas` v1.5.13
* Use `tmz/core` v1.2.10
* Use `tmz/schemas` v1.0.5
* Use `triniti/schemas` v1.0.5


## v1.1.17
* Add `site_section` and `site_sub_section` defaults to `/beta/` route.


## v1.1.16
* Add additional sizes in `renderAdsFlow` so adops can target custom sizes for zergnet _native_ ads.
* Use `tmz/core` v1.2.9


## v1.1.15
* Downgrade `beberlei/assert` to `v3.2.1` since it requires extensions that are not enabled in our .ini files


## v1.1.14
* Use `tmz/core` v1.2.8
* Use `tmz/schemas` v1.0.3
* Use `triniti/schemas` v1.0.3


## v1.1.13
* issue #1153: Revert committed work for #1153 and moved from server side to client side along with some code clean-up.
* issue #1170: Update App-ads.txt
* issue #1175: add experiment name in `cust_params` on all Ad Calls and change the VWO read-more variant URL to `/beta`.
* issue #1183: Add Teads (ad special div `<div id="ad-permalink-content1" class="ad-permalink-content1"></div>` to article permalink)


## v1.1.12
* Upgrade docker base image (201908) from `wb/php:0.4.0` to `wb/php:0.4.1`


## v1.1.11
* issue #1153: Pass new ad value into cust_params
* issue #1170: Update App-ads.txt
* issue #1174: [Ad] Add Pubmatic to Header Bidding
* Use `tmz/core` v1.2.6


## v1.1.10
* issue #1163: bug: Blocks that require dom manipulation need to have unique dom id's
* issue #1172: Adjust Single Poll Render On Desktop & Tablet


## v1.1.9
* issue #1076: Create "Read More" Experiment on Desktop/Tablet Homepage
* Use `tmz/core` v1.2.4.


## v1.1.8
* issue #1117: Update Spotlight Partner Styling. (Modification to v1.1.7)


## v1.1.7
* issue #1117: Update Spotlight Partner Styling.


## v1.1.6
* issue #1102: Remove links from TMZ Newsroom Today Promo.
* issue #1117: Update Spotlight Partner Styling.
* issue #1120: Update app.ads.txt file.
* issue #1129: Sports article permalink not using sports section.
* issue #1135: Update "Launch Doc" Styling on Mobile.
* issue #1154: Update ads.txt File.


## v1.1.5
* issue #1105: External Sponsorship Adjustments (adjustments)
* issue #1106: Advertorial Sponsorship Adjustment (adjustments)
* issue #1108: Internal Sponsorship Adjustments (adjustments)


## v1.1.4
* issue #1105: External Sponsorship Adjustments (adjust markup)
* issue #1106: Advertorial Sponsorship Adjustment (adjust markup)
* issue #1108: Internal Sponsorship Adjustments (adjust markup)


## v1.1.3
* issue #1105: External Sponsorship Adjustments
* issue #1106: Advertorial Sponsorship Adjustment
* issue #1108: Internal Sponsorship Adjustments


## v1.1.2
* Move all cache back to elasticache.  Performance testing didn't show that local redis helped at all.
* issue #1104: Sponsored by is removing the SEO TITLE and or TITLE from the articles.
* issue #1110: Video Blocks Should Be Able To Autoplay In Blocks On Blogroll.
* issue #1111: Implement App-Ads.txt.


## v1.1.1
* Move FPC cache to elasticache along with NCR.
* Change json linked data publisher logo to use `tmz-logo-red-147x60-v1.png` because google seems to not like the transparency.
* issue #1063: If User Is Staff Unpublished Videos Should Display And Be Playable.


## v1.1.0
* Use redis persistent connections.
* Redirect any .php urls to home page as they are all invalid.
* issue #1019: bug: Second to last image on every gallery has issues with not rendering, or showing up blank.
* issue #1050: Linktracker service uses window.open for external links and requires double click on safari.
* issue #1059: Fixing support for new ids in old photos url format
* issue #1063: If User Is Staff Unpublished Videos Should Display.
* issue #1067: Add dimensions for publisher logo.
* issue #1083: Update Launch Gallery icon on Mobile.
* issue #1085: Update ads.txt File.


## v1.0.18
* Redirect old URIs with junk after the article route in the vhost.


## v1.0.17
* Add ddos redirect rule to get the mutant uuid off root requests which are all junk.


## v1.0.16
* issue #997: BUG: The banner prompting the user to install the TMZ app does not appear if the user navigates to www.tmz.com on smartphone and doesn't already have the TMZ App installed.
* issue #1036: Articles From 6/26/19 and Earlier Should Not Receive Dynamic Launch Quotes for Galleries But Always Display Credit.
* issue #1047: Adjust Poll Design To Match Old Styling.
* issue #1048: If User Is Staff Unpublished Galleries Should Display And Be Viewable.
* issue #1055: Bug: Poll Percentages are going above 100% when voting.
* Remove all `robots_enabled` flags check.


## v1.0.15
* issue #1043: BUG: Polls in galleries are sometimes displaying incorrect percentages.
* issue #1051: Document Compatibility Mode Tag position is set too low.
* issue #1039: In Article Schema for image objects, please remove width and height references.
* Show full comment count for all comment number.


## v1.0.14
* issue #1040: Facebook Engagement Should Only Display To The Tenth Instead Of The Hundredth.
* Allow staff user to see unpublished galleries in article permalink.
* Increase `realpath_cache_ttl` in `php.ini.tpl` from 600 to 43200.


## v1.0.13
* Use `triniti/news` v1.0.6 with slotting fix.
* Use `tmz/schemas` v1.0.2
* Use `triniti/schemas` v1.0.2
* Test with `--classmap-authoritative` in `provisioning/codebuild/build.sh` for possible performance improvement.


## v1.0.12
* issue #1034: Update Treatments Should Render With PT timezone instead of PDT or PST.


## v1.0.11
* issue #1031: Add X-Robots-Tag HTTP header to all ajax routes.
* Fix invalid date format for json linked data, use IS08601 zulu.
* Update to slotting cache so they share the same namespace as api (for faster updates).


## v1.0.10
* Ensure is_staff is always in render context.
* Do not render a block at all (not even its container) once a page break has rendered.


## v1.0.9
* issue #1021: Bug: Slotting An Article Places It In The Wrong Slot. (add slot info to health check for debugging)
* Fix logic in determining when update date/time renders on blocks.  Convert both to same timezone.


## v1.0.8
* issue #1021: Bug: Slotting An Article Places It In The Wrong Slot.


## v1.0.7
* issue #1028: Polls Design Adjustment.
* issue #1016: Fix simple.xml feed only returning homepage articles.
* issue #1022: When user 'Is Staff' load no ads on article preview.
* issue #1017: Update ads.txt File
* issue #1023: Vilynx attribute is using wrong identifier.
* issue #1024: Articles From 6/26/19 and Earlier Should Not Receive Dynamic Launch Quotes for Galleries.
* issue #988: Category listing "Read More Stories" link isn't loading more stories.


## v1.0.6
* issue #1007: A grid-like image is briefly displayed before displaying the first image in the gallery on smartphone.
* fix text block updated date timezone bug


## v1.0.5
* fix social count css


## v1.0.4
* issue #995: fix for lightbox freeze after very rapidly attempting to change slides
* issue #994: Slider ellipsis css fix.
* issue #1000: Related Articles need margin fix below 767px.


## v1.0.3
* issue #984: "v new poll" not reporting votes as expected
* issue #987: Gallery thumbnail too large if only 1 gallery in footer of end card.


## v1.0.2
* Style tweaks and refinements by Sputnik.


## v1.0.1
* Add the ad size classes to unrendered ad slots that are referencing already placed divs.


## v1.0.0
* Initial stable version.
* issue #962: smartphone - very long search string allows results page to scroll horizontally
* fix weird iPhone 6+ iOS 9.3.4 video block bug
* remove www2 for our base url, now it's just www!


## v0.12.24
* issue #202: gallery updates


## v0.12.23
* issue #202: Reverting turbolinks replaceState
* issue #924: Clicking on the comments icon under the title in the article does not take you to the comments section on microsoft Edge and Safari
* issue #925: Add MS Edge keyCode support for gallery slider and lightbox.
* issue #927: Render HTML in gallery captions
* issue #931: When inside an article on ipad, Clicking the Comments button in the articles title causes the entire article to go opaque.(Greyed out)
* issue #932: Update Ads.txt file for Desktop & mWeb
* issue #933: iOS Chrome: The user isn't taken to the Apple Podcast app if the user selects the "Listen on Apple Podcasts" button
* Whenever a query for most recent videos is needed, use the tmz trending category ref.


## v0.12.22
* issue #909: Make requests for gallery polls as they're needed rather than when the gallery first loads
* issue #898: TV Listings Issues (again)
* turbolinks replaceState


## v0.12.21
* Don't cache the response when posting a vote so the resulting vote count is more fresh.
* issue #898: TV Listings Issues
* issue #878: The title of the latest three galleries isn't underlined when the user hovers their mouse over them on the Photos Page.


## v0.12.20
* issue #887: Video permalink issues
* fine tune gallery css


## v0.12.19
* Eliminate prebid down to the bare metal then rip its unit faces off completely because if you don't it WILL continue to bid those fuckers. Use the leftover skeleton power to rebuild a new set of units.
* adjust some text sizes in lightbox end card


## v0.12.18
* do not refresh all ads on gallery permalink, just the corner.


## v0.12.17
* issue #202: Gallery close not tracking page view
* issue #876: fix social buttons on article permalinks
* issue #878: css gallery title fix
* when ads that have been shuffled come back into viewport, refresh ads


## v0.12.16
* Append "Show" to show page html titles.
* Use `pbj.get('title', html_title)` for page title in `base.html.twig` loadPage so analytics reflect's the node's title, not the html title.
* Ensure infinite blogroll and load widget don't dispatch renderAds at all if it has no unrendered slots.


## v0.12.15
* Increase elasticsearch query timeout to 250ms to ensure complete results are returned even in spikey conditions.
* show/hide kaltura share button without dom manipulation
* issue #802: changing lightbox slides with keyboard can affect sidebar gallery widget


## v0.12.14
* issue #854: ensure youtube blocks are always correctly styled
* issue #202: wait for gallery to be available before calling first smartphone `slide_rendered`


## v0.12.13
* issue #175: tmz-live e2e, fix episode highlights gradient


## v0.12.12
* issue #795: The controls and content of an audio block aren't appearing when navigating between pages.
* issue #175: tmz-live e2e, fix Vilynx hover
* disable omniture s.Media.autoTrack in yet another place


## v0.12.11
* Fix redis config namespaces so all apps share same ncr keys.


## v0.12.10
* update kaltura configs and fix unhandled share button rejection and smartphone photo permalink.
* Simpler redis config and reduced retry interval for redis.


## v0.12.9
* assorted video plugin updates
* Fix bug in renderAdsFlow when no ad size has been set on a slot.


## v0.12.8
* enrich ads for primary people as well as regular people
* Dynamically add `ad-size-${slot.size}` to dynamically targeted ad divs (like ad-blogrollN).
* Do not refresh all ads on the page when infinite scrolling occurs, just render the ads that haven't rendered yet.
* Disable analytics dataLayer push when the page node is not published.
* Disable ads, sharing and analytics on video players when the video is not published.
* issue #845: ad spacing and minimum heights.


## v0.12.7
* add some fpc debugging2


## v0.12.6
* preserve video caption settings across new media/reconstructed players
* add some fpc debugging
* add blocks and kaltura_flavors to censor pbj as we don't need it on the client.


## v0.12.5
* issue #736: Update ads.txt file for Desktop & mWeb
* issue #837: Remove Ads From Preview Pages.
* kaltura debug


## v0.12.4
* issue 748: blogroll widget e2e. Update primary block render method.
* Increase prod-hot Memory from 2048 to 4096 since it is required when using Cpu 2048.
* Add turbolinks-cache-control meta tag because reasons.


## v0.12.3
* Disable kaltura omniture autoTrack.
* Increase prod-hot Cpu from 1024 to 2048 to see if this gets us back under 100ms.
* Increase `gdbots_ncr.ncr_search.elastica.query_timeout` from 50ms to 150ms.


## v0.12.2
* Add `/.well-known/amphtml/apikey.pub` the enable amp cache bust.
* issue #749: loadmore button dispatch double action.
* update vilynx redirect text for when video is not going to play inline
* issue #770: mobile button hover states
* issue #771: spotlight widget should open a regular browser
* issue #797: Facebook embeds are extending past the right side of the device screen on smartphone.


## v0.12.1
* In blogroll_permalink canvas blocks, don't extend the main block since it has logic to hide/show based on page breaks and permalink.


## v0.12.0
* Update `_disqus.html.twig`. Show comments automatically in permalink if user clicks the comment icon in blogroll.
* issue #748: blogroll e2e. Adjust permalink blogroll widget.
* issue #175: show :: tmz-live e2e (is_live treatment on smartphone)
* Use `tmz/schemas` v1.0.0
* Use `triniti/schemas` v1.0.0
* video analytics


## v0.11.38
* issue #175: show :: tmz-live e2e (is_live treatment, renderComponent when is_live)
* issue #175: show :: tmz-live e2e (padding for tablet, vylinx poster)
* issue #749: Fire page view tracking when load more or infinite scroll happens
* tweak tmz-live playlist widget for live stream and evergreen content (cta)
* issue #785: seo :: remove multiple h1 from articles


## v0.11.37
* issue #675: hero bar widget e2e (padding for tablet)
* issue #632: video e2e (analytics)
* fix sticky header for edge


## v0.11.36
* issue #693: video permalink e2e
* issue #174: tmz-on-tv show page e2e, styling
* Add kalturaDebug function to base so we can use it to debug kaltura players with trackEventMonitor.


## v0.11.35
* issue #632: video e2e (vilynx styling and config)
* issue #202: gallery e2e (history issues)
* issue #629: channel permalink e2e (styling)


## v0.11.34
* Update babelrc. Add `ios_saf 10` and `firefox 15` to support list.
* issue #202: gallery e2e (history issues)


## v0.11.33
* start gallery blocks on slide of poster image if that image is in gallery
* preserve video audio settings across destroy/recreate
* issue #748: blogroll e2e (adjust permalink blogroll widget)


## v0.11.32
* issue #689: gallery permalink e2e (adjust close icon svg)
* issue #740: prevent twitter-tweet-block from rendering twice
* use youtube nocookie domain, skip consentsTo for that block


## v0.11.31
* issue #695: Add Podcasts Section.
* issue #707: Adding kaltura configs per environment.
* issue #722: Hide vilynx poster on tmz-live page
* issue #723: Do not add swipe to image block in smartphone view.
* use lg size for gallery images
* issue #722: Hide vilynx poster on tmz-live page
* upgrade prebid from v2.15.0 to v2.17.0
* issue #202: gallery e2e (prevent new slides from breaking lightbox animation)
* issue #689: gallery permalink e2e (Chris' feedback)


## v0.11.30
* issue #643: Playlist widget e2e: fix adsEnabled param
* issue #707: Adding kaltura configs per environment.
* issue #632: video player e2e
* issue #202: gallery e2e (more ios scrolling, history entries)
* issue #693: video permalink e2e (correct noopener noreferrer)
* issue #689: gallery permalink e2e (disable lightbox on timeline permalink)
* change "watch tmz" nav link to point to tmz-on-tv show page


## v0.11.29
* issue #688: Kaltura s code
* issue #174: tmz-live show page e2e
* issue #175: tmz-on-tv show page e2e


## v0.11.28
* Add podcasts stubs.
* In `renderAdsFlow` set enableSendAllBids in prebid back to true.


## v0.11.27
* fix lightbox gallery gumgum logic
* renderAds on every sidebar un/shuffle


## v0.11.26
* Use `tmz/schemas` v0.7.8
* Add support for ipv6 in schemas (mainly ctx_ipv6).
* issue #618: video player e2e (adsEnabled prop for video, use to disable ads in header)
* issue #674: slider widget e2e.
* issue #202: gallery e2e (differerent ios scrolling solution)
* only show tmz-newsroom image once video play has ended
* issue #673: Homepage – Refresh Homepage & Channel Pages After 5 Minutes of Inactivity
* tmz-on-tv e2e - showtimes, no listings message
* issue #683: GTM error if auth is not present


## v0.11.25
* issue #618: sidebar disappears when scrolling down the page then back up
* Don't clear out adSlots state in `renderAdsFlow.js` since it's causing ads to not render.  duh.
* Use Albert's Famous "Get More Like This Query" thingy for end cards. Let's see if it works.


## v0.11.24
* add video end card analytics and fix timing of launch text footer hiding
* issue #202: gallery e2e (properly prevent scrolling body when smartphone gallery is open)
* tmz-on-tv e2e - video player update


## v0.11.23
* Fix the promises promises, you knew you'd never catch, like in renderAdsFlowMax.
* issue #146: permalink e2e
* issue #632: video player e2e


## v0.11.22
* issue #202: gallery e2e - fix issues
* playlist widget e2e - update document title on video change
* tmz-on-tv e2e - video player and full episodes fixes


## v0.11.21
* Guard robots with flag so we can use www2 for testing.
* gallery e2e - adjust gallery lightbox css so it fades out properly


## v0.11.20
* gallery e2e - wait until corner ad div exists before rendering ad.
* issue #154: left align category title.
* issue #643: playlist widget e2e, fix endcard issue


## v0.11.19
* issue #628: disable lightbox on photos landing page.
* issue #202: gallery e2e
* issue #627: timeline permalink e2e
* analytics for fallback video


## v0.11.18
* Use `tmz/schemas` v0.7.7


## v0.11.17
* issue #480: Fix for kaltura s-code
* hash image paths
* issue #175: tmz live route :: desktop/tablet
* issue #603: Bug: Menu bar/header is disappearing/distorting when visiting the site for first time or in incogneto mode.
* issue #614: Bug: Gallery end card in smartphone view causes it to crash.
* issue: Fix bug: Infinite blogroll content being fetch twice.
* videos (wip)


## v0.11.16
* more renderAdsFlow debugging to find out what's wrong with prebid targeting delays.


## v0.11.15
* upgrade prebid to v2.12.0


## v0.11.14
* issue #563: articles :: ensure schema meets best practice
* issue #564: videos :: ensure schema meets best practice
* Don't use the document prebid `pbjs.removeAdUnit([])` since it doesn't work, instead of `pbjs.removeAdUnit('string')` for each unit.


## v0.11.13
* exclude sitemaps with no documents.


## v0.11.12
* issue #423: Implement disqus on article permalink (address issues)
* Reference all sitemap indexes directly from robots.txt.


## v0.11.11
* Combine sports sitemap news into regular sitemap news.


## v0.11.10
* issue #218: setup sitemaps (add "today" index)


## v0.11.9
* issue #218: setup sitemaps


## v0.11.8
* Resolve persistent cache in fpc.


## v0.11.7
* issue #558: For 404s, redirect if there exists a redirect URI.
* issue #567: playlist widget requirements for newsroom datasource.


## v0.11.6
* issue #567: playlist widget requirements for newsroom datasource
* gallery updates - render ad on mount, remove unnecessary getGallery action and endpoint
* defer requesting end cards/infinite images until end of galleries
* issue #555: Change the Date to the month/day/year format.
* issue #533: Add a print for articles.


## v0.11.5
* issue #508: Mobile site Menu Slider is not working appropriately
* issue #504: sub-asset video :: tracking issues
* issue #528: showtimes bugs
* issue #529: Create service for gallery lightbox
* dont load gallery block gallery via data attribute
* issue #537: right rail should repeat even before user loads more stories
* issue: #532: Add rel with value of noopener to all anchor links with target value of blank.


## v0.11.4
* Fix broken CategoryController.


## v0.11.3
* simpler lightbox getIntendedGalleryRefs
* issue #520: BUG: The Swipe isn't getting applied if the first block is a YouTube block.
* issue #478: link enchrichment
* issue #52: hide alert widget without animation
* fix showtimes after renaming `tmz` -> `tmz-on-tv`
* issue #404: Add analytics for galleries (address issues)
* issue #490: Sticky nav not showing up.


## v0.11.2
* issue #52: alert widget fix
* issue #404: Add analytics for galleries (address issues)
* fix infinite lightbox bug for galleries with 3 images
* issue #210: rss feeds (fixing issues)


## v0.11.1
* issue #467: hamburger nav not working consistently on tablet.
* issue #466: navigating between sections on a tablet does not load nav
* issue #404: Add analytics for galleries
* Fpc with redis.
* video player (wip)


## v0.11.0
* issue #127: video permalink route :: smartphone playlist player
* issue #335: update styling treatment for update_dates to encomass single wrapping updated element for all update_dates.
* issue #448: a large block of white space is present between the video block and the next block in the article when the user plays the video.
* issue #459: BUG: Update blocks with the same time but different date will get the "same update timestamp" treatment.
* issue #210: rss feeds
* issue #466: navigating between sections on a tablet does not load nav


## v0.10.5
* Add people purple permalink.
* Add some redirects for legacy routes.


## v0.10.4
* Bug fix on article permalink and some general widget cleanup.


## v0.10.3
* issue #439: Facebook share not displaying login.
* issue #608: Update gallery block to display launch text if present.
* issue #430: Bug: Content in the swipe field isn't getting applied to primary video.
* issue #439: Facebook share not displaying login.
* issue #431: Sports articles permalink ui fix.
* Fix bug for infinite blogroll won't load promotion slot.
* Check slotting key before assign new cursor.
* Use correct timeline badge for sponsor in blogroll.
* Use `tmz/schemas` v0.7.3


## v0.10.2
* More unit tests fixes.


## v0.10.1
* Client js bug and lint fixes!  f___ing sinon package again!


## v0.10.0
* issue #304: Enrich links
* issue #410: The content in the Swipe field is getting placed at the top-left of the primary image, where the content in the Soft Swipe should be.
* issue #252: video-block - PART 2
* issue #126: video permalink
* issue #305: gallery widget (wip)
* issue #178: tmz sports route


## v0.9.0
* issue #236: playlist-widget :: desktop/tablet
* issue: #409: implement heading block
* Use `tmz/schemas` v0.7.0
* Use `triniti/schemas` v0.15.0
* Use `triniti/canvas` v0.6.1 with new next_pbj spice and template finder.
* Make `AbstractController` for this project to share some common controller features.
* Eliminate use of `SiteTheme` it's gone.
* Caching improvements from tmz/core.


## v0.8.3
* Caching and lazy loading updates from tmz/core.


## v0.8.2
* Hot fix for frozen poll stats.
* issue: #335: Updated date template adjustment.


## v0.8.1
* Hot fix for poll voting and blogroll widget.


## v0.8.0
* issue #130: poll-grid-block (wip)
* issue #186: contact us/tips links
* issue #317: move vwo placement out of tag manager
* issue #305: gallery widget (wip)


## v0.7.2
* Take out 💩 all in gallery permalink.


## v0.7.1
* issue #62: blogroll widget :: desktop/tablet - infinate scroll
* issue #343: Played Kaltura Video Become Unresponsive When Moving To Another Page
* issue #340: enable show item CTA text on media-list widget
* issue #345: fix spotlight-widget footer
* issue #305: gallery widget (wip)


## v0.7.0
* issue #252: video-block (wip)
* issue #52: alert-widget (wip)
* issue #112: spotlight-widget
* sidebar disappearing on chrome desktop
* issue #106: poll-block (wip)


## v0.6.1
* Adjust listener so www and www2 will work in production.


## v0.6.0
* Use `tmz/schemas` v0.5.1.
* Article slotting (wip)


## v0.5.1
* Minor fixes on renderAdsFlow so we can get AdOps testing.


## v0.5.0
* Upgrade docker base image from `wb/php:0.2.0` to `wb/php:0.3.0`
* issue #54: carousel widget :: desktop (wip)
* issue #91: gallery-block (wip)


## v0.4.11
* Use new `/tmz-infra/*` ssm parameters in docker, codebuild, etc.


## v0.4.10
* Formating block debugging.
* General cdo in preview.


## v0.4.9
* Fixing bugs with NcrRequestDeceptercon not correctly NcrRequestInterceptoring based on staff awareness.
* unmount react on turbolinks click
* issue #298: review styles for preview page


## v0.4.8
* When I grow up I'm going to <strike>bovine university</strike> cmsu.
* issue #90: document-block
* Add preview endpoint for articles.
* issue #101: page-break-block


## v0.4.7
* issue #114: slider-widget :: tablet
* issue #115: slider-widget :: smartphone
* issue #120: spotify-track-block
* Customize ad unit path per environment/device in `renderAdsFlow` saga per adops.
* Add title to page object provided to loadPage.
* Add device_view to ad targeting params.


## v0.4.6
* Misc links cleanup in twig.
* Add `buffers.dropping(10)` to `RENDER_ADS_REQUESTED` channel.
* issue #488: BUG: YouTube and Facebook Video blocks will sometimes pop out of the main column on the homepage and in articles.
* issue #87: audio-block


## v0.4.5
* Convert loadWidget to thunk and dispatch renderAds if there are unrendered ads.
* Add renderedAt property to adSlots in redux so we can ensure we don't re-render ads too fast.
* Fine tune slider-widget and gridler-widget.
* Stub CategoriesController and render render blogroll or gridler depending on content type.


## v0.4.4
* issue #85: article block
* issue #114: slider-widget :: tablet
* issue #115: slider-widget :: smartphone
* issue #256: showtimes widget part 2 :: desktop/tablet
* issue #271: add poster image to soundcloud audio block
* issue #273: upgraded bootstrap to 4.3.1
* Use `tmz/schemas` v0.4.5.


## v0.4.3
* revert dependency upgrade


## v0.4.2
* issue #70: vimeo video block
* issue #123: soundcloud audio block
* issue #111: showtimes widget :: desktop/tablet
* issue #148: youtube-video-block
* Stub prebid and renderAdsFlow.
* Use `triniti/dam` v0.3.8.


## v0.4.1
* Add a QA testing route `/_/qa{site_section}/` and `site_section` is optional and can be any slug which will be used to prefix all promotion slots.


## v0.4.0
* Turn off xfbml parsing and instead parse them directly once we render them.
* Remove docker build debug on container boot.
* Enable some temp debugging on FpcKernel.
* Add temp benchmarking to Aws credentials provider.
* Add vilynx_enabled flag check in `AppExtension` before returning an id because their script sometimes breaks shit.
* issue #168: Switch ECS configuration to use Fargate.


## v0.3.2
* Do not persist the BUILDING_IMAGE arg in Dockerfile.


## v0.3.1
* Attempt to fix symfony boot/prime error by ensuring all `app_*` and `cloud_*` are referenced by environment and not accidentally baked into the kernel's juicy chicken, now available at your local KFC.


## v0.3.0
* issue #77: implement facebook-video-block for all device views.
* Fpc improvements (pass through etag) and less backend validation.
* Symfony optimus priming on roll out with new all spark cloud provider as environment.
* Update `triniti/canvas` to v0.6.0 with new template structure and `render['block-name']` map variable.


## v0.2.18
* issue #83: gridler widget :: desktop/tablet
* issue #84: gridler widget :: smartphone
* issue #118: tetris widget :: desktop/tablet
* Add FpcKernel and enable ESI.
* Maybe fix webpack font references when running with cdn. Maybe. ლ(ಠ益ಠლ)
* issue #108: media-list widget :: desktop/tablet


## v0.2.17
* cleanup facebook-post-block code
* issue #45: implement twitter-tweet-block
* issue #50: google-map-block :: desktop
* issue #74: google-map-block :: smartphone
* issue #28: Sticky Right Rail on Homepage & Category Pages
* issue #79: instagram-media-block :: desktop/smartphone


## v0.2.16
* Update `gdbots/ncr` to v0.3.12 with bug fix for node slug lookup cache.


## v0.2.15
* Use `tmz/schemas` v0.4.4.
* Change `imagez[.env].tmzlabs.com` to use `dam[.env].tmzlabs.com` until akamai is fixed up.
* issue #223: route :: setup pages route


## v0.2.14
* Stub linkTracker service in client so we can push events into gtm dataLayer. Example: `<a href="{{ pbj_url(node, 'canonical') }}" class="js-track-link" data-node-ref="{{ node_ref }}" data-widget-ref="{{ widget_ref }}">`.
* Use new `ScalingId` in cloudformation template so we can scale differently based on hotness.
* issue #49: code-block :: desktop/tablet


## v0.2.13
* issue #36: app shell footer :: tablet
* issue #136: quote-block :: desktop/tablet


## v0.2.12
* css refactor fix


## v0.2.11
* issue #46: canvas blocks: iframe-block
* issue #75: Desktop :: Facebook post block
* issue #96: hero bar widget :: desktop/tablet
* issue #118: tetris widget :: desktop/tablet
* issue #134: text block :: desktop
* issue #135: text block :: smartphone


## v0.2.10
* Remove dev config `web_profiler`


## v0.2.9
* Use docker image tag `wb/php:0.2.0`
* Add htmlImport and htmlImportLazy utils to client app. Can be used with html as well `<div id="a-div-id" class="js-html-import-lazy" data-url="/some-relative-url/">placeholder</div>`.
* Add ncr preloading for client side app.
* issue #103: consentsTo() fill in.
* issue #32: Desktop App Shell Navigation


## v0.2.8
* LMAO, RESOLVE the invalid `CLIENT_PUBLIC_PATH` when in AWS.


## v0.2.7
* Resolve invalid `CLIENT_PUBLIC_PATH` when in AWS.
* Move resolved pbj twig templates to pbj folder to differentiate them from other twig templates which are more explicitly referenced in controllers.
* Stub more of the pageview js and add some notes about strategies we'll use.


## v0.2.6
* Tracer bullet for client application and its deployment.


## v0.2.5
* Update HealthCheckPath in cloudformation from `/health-check` to `/health-check/`.


## v0.2.4
* Use `tmz/schemas` v0.4.1.
* Use `gdbots/query-parser` v0.3.1 with fix for invalid string casting on Numbr in ElasticaQueryBuilder.
* Add widgets for ad, carousel, code, gridler, hero-bar, media-list, showtimes, slider, spotlight, tag-cloud and tetris.


## v0.2.3
* Update composer.json version to correct release number


## v0.2.2
* Update "triniti/canvas" in composer.json from "dev-render-blocks as 0.4.1" to "^0.5".


## v0.2.1
* !GetAtt 'Service.Name' does not return the correct value.  Use a Select|Split workaround.


## v0.2.0
* update to tmz/schemas 0.1.7


## v0.1.4
* Change health-check on TargetGroup to HTTP as well.


## v0.1.3
* TargetGroup in `provisioning/codebuild/cloudformation.yaml.tpl` should be HTTP as we're not putting the cert into the container.


## v0.1.2
* Use shared HTTPS listener provided by tmz-ecs infrastructure.


## v0.1.1
* Use HTTPS for `AWS::ElasticLoadBalancingV2::TargetGroup` and `AWS::ElasticLoadBalancingV2::Listener` in `provisioning/codebuild/cloudformation.yaml.tpl`.


## v0.1.0
* Initial version.
