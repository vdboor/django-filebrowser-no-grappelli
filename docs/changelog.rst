:tocdepth: 1

.. |grappelli| replace:: Grappelli
.. |filebrowser| replace:: FileBrowser

.. _changelog:

Changelog
=========

3.6.2 (not yet released)
------------------------

* New: Compatibility with Django 1.9
* New: Better test coverage with tox.
* New: Improved tests.
* New: Add support for using filebrowser from tiny-mce v4
* Fixed: The block usertools not displayed on django 1.8
* Fixed: Fix url tag for django 1.4
* Fixed: Django styles for experimental FileBrowseUploadField

3.6.1 (September 9th, 2015)
---------------------------

* Compatibility with Django 1.8

3.5.8 (November 8th 2015)
--------------------------

* New: Sort by multiple attributes.
* Improved: Add back button from upload page.
* Improved: Show url after upload
* Improved: Update video extensions for common HTML5 video types.
* Improved: Improved Python 3 compatibility.
* Improved: Version size with crop.
* Improved: Fix cannot write mode P as JPEG.
* Fixed: Action pulldown with all documents (not only images).
* Fixed: Version scaling with fixed width and auto height (added tests as well).
* Fixed: Compatibility with Django 1.4.
* Fixed: Management command when generating all versions (fb_version_generate).
* Fixed: Home link with breadcrumbs.
* Fixed: Removed cycle templatetag (for compatibility with Django 1.4 to 1.7).

3.5.7 (December 14th 2014)
---------------------------

* New: Compatibility with Django 1.7.
* Improved: Updated tests because of the new random suffix with get_available_name (django storage).
* Improved: Added an icon in order to mark finished uploads.
* Improved: Show resulting filename (e.g. with suffix, converted) after successful upload.
* Fixed: Permissions with file upload.
* Fixed: Unified json response with _upload_file (no matter if file already exists or not).

3.5.6 (August 16th, 2014)
------------------------

* New: Add fake model to show filebrowser in admin dashboard
* New: Make fake model optional
* Improved: Restore the filebrowser icon for file fields.
* Improved: Escape extension dots in default EXCLUDE list, avoid empty entry
* Improved: Set xframe_options_sameorigin policy on filebrowser views.
* Fixed: Fix filebrowser button for newly added inlines

3.5.5 (April 13th, 2014)
------------------------

* New: Added client-side (JavaScript) file extension validation to the AJAX uploader.
* New: Added experimental Python 3.3 support.
* Improved: Tests with convert/normalize (removed special chars from test filename).
* Fixed: File selection after using search box (CKEditor).
* Fixed: Removed encoding of file URIs with CKEditor.

3.5.4 (February 21st, 2014)
---------------------------

* Fixed: Placeholder functionality (including tests).
* Fixed: Convert/normalize filenames (including tests).
* Fixed: Handling uppercase extensions with browse.

3.5.3 (January 7, 2014)
-----------------------

* New: added ``path_full`` to FileObject.
* Improved: added docx to EXTENSIONS.
* Improved: Recommend pillow instead of PIL as a requirement.
* Improved: Added additional test cases.
* Improved: Updated documentation.
* Improved: Consistent use of storage (e.g. storage.location, storage.url).
* Improved: Removed unnecessary functions (e.g. url_join, url_strip).
* Improved: Moved sort_by_attr to FileListing.
* Improved: Regex matches with file versions on browse.
* Improved: Using django.conf.urls (with django.conf.urls.defaults as fallback).
* Improved: Adding CONTRIBUTING.rst.
* Improved: Removed static Media inner class with fields.
* Improved: Removed search icon with fields (has not being used).
* Improved: Added custom class attributes with filebrowser field.
* Improved: Updated translations.
* Fixed: fixed exception handling with python 2.5.
* Fixed: fixes dir with SEARCH_TRAVERSE true and version select.
* Fixed: Make Django FileUploadHandlers work (also fixed a memory leak).
* Fixed: return correct filename with ``OVERWRITE_EXISTING``.
* Fixed: fb_version_generate with ``FILEBROWSER_VERSIONS_BASEDIR``.
* Fixed: Table sorting with asc/desc.
* Fixed: Added DeprecationWarning for ``FileObject.directory`` and ``FileObject.folder``.

3.5.2 (February 22, 2013)
-------------------------

* Fixed: Use placeholder with version_generate (not only templatetags).
* Fixed: translate extension group name in upload form.
* Fixed: updated filter dropdown HTML.
* Fixed: Make setup.py work with Python 3.
* Fixed: File submit with search traversal.
* Fixed: Fixed fileobject path with Windows.
* Improved: Throwing an exception when in DEBUG and version is not generated (with using the templatetag).
* Compatibility with Django 1.5.

3.5.1 (November 09, 2012)
-------------------------

* Fixed: Documentation with Signals.
* Fixed: File Upload using basic submission.
* Fixed: Added site instance to Signals.
* Improved: Don't hide errors during generate-command.
* Improved: Follow symlinks with generate-command.
* Improved: Added some translations (e.g. for "Upload File").
* New: Setting OVERWRITE_EXISTING.
* New: Added file ``signals.py``.
* New: Support for Django 1.5.

3.5.0 (July 20, 2012)
---------------------

* Compatibility with Django 1.4 and Grappelli 2.4.

3.4.3 (20.6.2012)
-----------------

* Fixed a bug with versions not being generated (in case of capitalized extensions).

3.4.2 (26.3.2012)
-----------------

* Fixed security bug: added staff_member_required decorator to the upload-function.
* Fixed a XSS vulnerability with fb_tags.

3.4.1 (7.3.2012)
----------------

* Fixed an error with quotes (french translation) in upload.html.
* Updated translations.
* FileObject now returns path (with __unicode__ and __str__), instead of filename. This is needed because otherwise form.has_changed will always be triggerde when using a FileBrowseField.
* Fixed a bug with versions and "f referenced before assignment" (e.g. when an image is being deleted)
* Updated docs (warning that FILEBROWSER_MEDIA_ROOT and FILEBROWSER_MEDIA_URL will be removed with the next major release – use custom storage engine instead).
* Fixed issue with MEDIA_URL hardcoded in tests.
* Fixed issue when MEDIA_URL starts with https://.
* Fixed issue with default-site (if no site is given).
* Fixed bug with using L10N and MAX_UPLOAD_SIZE in upload.html.
* Fixed small bug with importing Http404 in sites.py.
* Fixed bug with Fileobject.exists.
* Added NORMALIZE_FILENAME.

3.4.0 (15/11/2011)
------------------

For further information, see :ref:`releasenotes`.
