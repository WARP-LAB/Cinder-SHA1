Cinder-SHA1
===


###About

Cinder block, that has no dependancies, for simple SHA1 hashing.


###Todo

* add exception throwing on any errors (especially when trying to checksum non existing file)

*Cinder comes with Boost which has `boost::uuids::detail::sha1` in `boost/uuid/sha1.hpp` and of course it works, but we find this small helper class more attractive for quick checksumming files downloaded from interwebs.*


###Example

```
fs::path pathToFile = getAssetPath("file.ext");

SHA1 mySha1;
string checkSum;
checkSum = mySha1.from_file( pathToFile.string() );
cinder::app::console() << "file checksum: " << checkSum << endl;

```

###License

Found randomly in interwebs, located in [pushover repo](http://pushover.sourceforge.net/repos/head/src/). All credit goes to as stated below.

    ============
    SHA-1 in C++
    ============

    100% Public Domain.

    Original C Code
        -- Steve Reid <steve@edmweb.com>
    Small changes to fit into bglibs
        -- Bruce Guenter <bruce@untroubled.org>
    Translation to simpler C++ Code
        -- Volker Grabsch <vog@notjusthosting.com>
