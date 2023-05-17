Pixlee PHP API Library
=================
This library is a simple API wrapper for Pixlee's v1 API. It allows you to get your albums, their photos, and the data associated with each. You can also add photos and videos to your albums. Borrows heavily from the Pixlee Ruby gem.


Installation
=================
This can be installed via Composer. Or you can include Pixlee.php in your source.

Usage
==================
$pixlee = new Pixlee(pixlee_api_key, pixlee_secret_key, pixlee_user_id)

**Getting  your albums**

$albums = $pixlee->getAlbums();

**Getting all photos in an album**

$photos = $pixlee->getPhotos(album_id, array( 'sort'      => 'recent', 
                                              'page'      => 2, 
                                              'per_page'  => 3
                                              ));

**Get individual photo**

$photo 	=	$pixlee->getPhoto(album_id, album_photo_id);

**Adding a new photo to an album**

$photo = $pixlee->createPhoto(album_id, array('photo_url'     => 'url_to_photo', 
                                              'email_address' => 'email_of_photo_owner', 
                                              'type'          => 'photo|video'
                                              ));
