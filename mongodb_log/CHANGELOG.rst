^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package mongodb_log
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.6.0 (2022-09-20)
------------------
* Ensure Python 3 compatibility in mongodb log (`#277 <https://github.com/strands-project/mongodb_store/issues/277>`_)
* update package.xml to format=3 (`#269 <https://github.com/strands-project/mongodb_store/issues/269>`_)
* Contributors: Gal Gorjup, Kei Okada, Nick Hawes

0.5.2 (2019-11-11)
------------------
* back to system mongo
* Contributors: Ferenc Balint-Benczedi, Nick Hawes, Shingo Kitagawa, Volker Gabler

0.5.1 (2019-06-28)
------------------

0.5.0 (2018-12-20)
------------------
* Merge pull request `#231 <https://github.com/strands-project/mongodb_store/issues/231>`_ from bbferka/melodic-devel
  Melodic devel
* back to system mongo
* Contributors: Ferenc Balint-Benczedi, Nick Hawes

0.4.5 (2019-06-28)
------------------

0.4.3 (2019-04-04)
------------------
* Merge pull request `#238 <https://github.com/strands-project/mongodb_store/issues/238>`_ from charlielito/patch-1
  Fix typo in log message
* Fix typo in log message
  It is subscribe rather than subsribe
* Contributors: Carlos Andrés Álvarez Restrepo, Nick Hawes

0.4.2 (2018-06-04)
------------------
* instead of lsb-release read /etc/os-version from CMake to find OS version
* Contributors: Ferenc Balint-Benczedi

0.4.1 (2018-05-29)
------------------
* check if env. var. exists if not decide based on OS version
* Contributors: Ferenc Balint-Benczedi

0.4.0 (2018-05-23)
------------------
* if compiler supports it use C++11
* Contributors: Ferenc Balint-Benczedi

0.3.8 (2018-05-02)
------------------

0.3.7 (2017-12-14)
------------------
* Merge pull request `#210 <https://github.com/strands-project/mongodb_store/issues/210>`_ from hawesie/kinetic-devel
  Updated to build on OS X with the mongo client legacy version.
* Used the openssl libs from find_package.
* Updated to build on OS X with the mongo client legacy version.
  This makes a couple of changes. For libmongocxx_ros the paths for openssl are added to the scons command and all ".so" and set to ".so" or ".dylib" depending on platform. For mongodb_log this removes the explicit linking of mongoclient which isn't needed since catkin_libraries includes the lib created by libmongocxx_ros.
* Contributors: Nick Hawes

0.3.6 (2017-09-14)
------------------

0.3.5 (2017-09-03)
------------------

0.3.4 (2017-09-03)
------------------

0.3.3 (2017-09-02)
------------------

0.3.2 (2017-08-31)
------------------

0.3.1 (2017-08-24)
------------------


0.3.0 (2017-08-24)
------------------


0.2.2 (2017-06-28)
------------------

0.2.1 (2017-06-28)
------------------

0.2.0 (2017-06-28)
------------------
* dependencies fixing
* Contributors: Marc Hanheide, Nick Hawes

0.1.30 (2017-06-23)
-------------------

0.1.29 (2017-06-19)
-------------------

0.1.28 (2016-11-09)
-------------------

0.1.27 (2016-11-01)
-------------------

0.1.26 (2016-10-14)
-------------------
* indigo-0.1.25
* Updating changelogs
* indigo-0.1.24
* updated Changelogs
* Contributors: Nick Hawes

0.1.25 (2016-04-28)
-------------------

0.1.24 (2016-04-19)
-------------------

0.1.23 (2016-04-19)
-------------------
* Fixed missing namespace for mongodb_log
* indigo-0.1.22
* updated Changelogs
* Contributors: Nick Hawes


0.1.22 (2016-02-23)
-------------------


0.1.20 (2015-11-11)
-------------------



0.1.19 (2015-10-28)
-------------------

0.1.18 (2015-10-28)
-------------------

0.1.17 (2015-09-01)
-------------------

0.1.16 (2015-08-04)
-------------------
* add option to treat topic name arguments as regular expression
* add option to specify collection name
* Contributors: Furushchev

0.1.15 (2015-05-10)
-------------------

0.1.14 (2015-04-27)
-------------------
* Adding install targets for mongodb_log
  Closes `#129 <https://github.com/strands-project/mongodb_store/issues/129>`_
* Contributors: Christian Dondrup

0.1.13 (2015-04-22)
-------------------
* Recheck topics at a fixed interval in order to attempt to resubscribe to topics that were missing at startup.
  This closes `#126 <https://github.com/strands-project/mongodb_store/issues/126>`_.
* Changed mongodb_log to not wait for topics to be published, instead subscribing to all the other topics
* Contributors: Nick Hawes, Nils Bore

0.1.12 (2015-02-09)
-------------------

0.1.11 (2015-02-09)
-------------------
* Extended usage output string by new command line options
* Changed default behaviour back to its former way
  The 'a' command line parameter now activates throttling; not specifying it makes the logger log all tf transformations.
* Added throttling capabilities for high-frequency tf logging
  Added tf logging throttling capabilities originally introduced in https://github.com/code-iai/ros-mongodb_log. A transform is only logged when either this transform has not been logged before, or when the new version of this transform is sufficiently different from the one logged before. Additional command line parameters can be used to control how throttling is done:
  * `-k <d>`: Cartesian (vectorial) distance (in meters) threshold between the old and the new transform
  * `-l <d>`: Angular diastance (in deg) threshold between the old and the new transform
  * `-g <d>`: At least log every transform every `d` seconds, even if nothing changed
  * `-a`: Always log, don't throttle
* Contributors: Jan Winkler

0.1.10 (2014-11-23)
-------------------

0.1.9 (2014-11-18)
------------------
* Use rospy to remove additional arguments when launched via roslaunch
* Contributors: Nils Bore

0.1.8 (2014-11-11)
------------------

0.1.7 (2014-11-09)
------------------

0.1.6 (2014-11-06)
------------------

0.1.5 (2014-11-05)
------------------

0.1.4 (2014-10-29)
------------------

0.1.3 (2014-10-21)
------------------

0.1.2 (2014-10-20)
------------------

0.1.1 (2014-10-17)
------------------

0.1.0 (2014-10-16)
------------------
* This adds latched recording and playback to the log and playback nodes.
  This is the final part of the functionality to close `#5 <https://github.com/strands-project/mongodb_store/issues/5>`_
* Added meta logging to other C++ loggers.
* Calling on correct document.
* Building up type processing knowledge.
* Adding meta information to C++-logged documents.
* Handlings strings which cannot be treated as UTF-8 as binary.
* Moved back to processes to test.
* Debugging ulimit issue.
* Contributors: Nick Hawes

0.0.5 (2014-10-09)
------------------

0.0.4 (2014-09-13)
------------------
* added libssl and libcrypto for ubuntu distros where this is needed due to the static nature of the libmongoclient.a
* Contributors: Marc Hanheide

0.0.3 (2014-08-18)
------------------
* Renamed rosparams `datacentre_` to `mongodb_`.
  Fixes `#69 <https://github.com/strands-project/ros_datacentre/issues/69>`_
* Renamed ros_datacentre to mongodb_store for to fix `#69 <https://github.com/strands-project/ros_datacentre/issues/69>`_.
* Contributors: Nick Hawes

0.0.2 (2014-08-07)
------------------
* Dynamically choose MongoDB API
  Use Connection if using an older mongopy, otherwise use MongoClient.
* Cleaned up boilerplate in mongodb_log package.xml
  Removed a bunch of XML comments (that came from the package.xml
  template) from the package.xml file. Added pymongo as a run dependency.
* Main process no longer calls init_node.
  This fixes bugs related to calling init_node multiple times in the same
  process. Main process now has its own signal handler for shutting down
  cleanly.
* Added 'inserted_at' meta with proper date object to logged data.
  This added compatibility with message store and also allows native date queries on results.
* Changes to how meta info is stored.
* Added boost filesystem for new version of ld.
* Added mongo dependency
* More benchmark removal
* REmoved rrd bits.
* Removing benchmarking stuff.
* Restructuring for new repo position.
* Moved all files into mongodb_log subdirectory for later inclusion in a broader package.
* Contributors: Alex Bencz, Christian Dondrup, Nick Hawes
