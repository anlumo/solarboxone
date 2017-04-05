lws-esp32-test-server-demos
===========================
## For use with lws-esp32-factory
This relies on setup capability provided by
https://github.com/warmcat/lws-esp32-factory
which runs from the "factory" partition on ESP32.  This app is
designed to run from the 2.9MB OTA partition.
## Build
Clone and bring in the lws submodule (it's unpatched lws master)
  $ git clone git@github.com:warmcat/lws-esp32-test-server-demos.git
  $ git submodule update --init --recursive
 $ make all flash_ota monitor
using lws-serial, eg, https://lws-1234 or https://lws-1234.local
 - The button at the bottom should reset you into the setup / factory app

 - The "War and Peace" demo should load the 4MB text from the 1.2MB gzipped zip
   file directly, using gzipped data to the browser.