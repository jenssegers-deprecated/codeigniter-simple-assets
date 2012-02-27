CodeIgniter Simple Assets
=========================

This will be the most simple asset helper you have ever seen. It is a wrapper around CodeIgniter's base_url() function with the addition of an asset group parameter.

Installation
------------

Copy the files to the corresponding folder in your application folder (or use spark).

Structure
---------

In your root, create a folder called assets with this structure:

    assets
    -- css
    -- img
    -- js
    
If you would rather work with asset groups you can use the following structure:

    assets
    -- fancy
       -- css
       -- img
       -- js
    -- mobile
       -- css
       -- img 
       -- js
    
Usage
-----

This helper is loaded using the following code:

    $this->load->helper('assets');
    
Or autoload it by adding 'assets' to the $autoload['helper'] array in the autoload.php file.

To get the url to your asset files you use the `asset_url()` function:

    <img src="<?php echo asset_url('img/logo.jpg'); ?>" />
    
This will load logo.jpg from the assets/img/ directory. If you decided to split your assets in groups you can use the extra optional group parameter:

    <img src="<?php echo asset_url('img/logo.jpg', 'mobile'); ?>" />