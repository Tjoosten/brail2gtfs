# NMBS/SNCB to GTFS scraper

Scrapes the Belgian railways and generates GTFS files for the current year.

If you're unsure what GTFS is, check the explanation at http://gtfs.org.

Following traintypes are included:
IC, ICE, L, P, TGV, THALYS, TRN and EXT

You can download a copy at: http://gtfs.irail.be/

## Install

We use the PHP package manager [composer](http://getcomposer.org). Make sure it's installed and then run from this directory:

```bash
composer install
```

## Custom configuration

You can configure the start_date, end_date, feed_version, language and train_types of the GTFS-files by changing config.php in your favorite editor.

## Generating the GTFS file

There are a couple of scripts in the scripts folder. Run them in order. The scraped results will be in the dist folder.

```bash
php scripts/*.php
```

Afterwards, go to the dist folder, and create a zip archive:
```bash
cd dist/
zip brail-0.1.zip *
# remove them for the next run
rm *.txt
```

Your NMBS/SNCB GTFS file is now ready for publishing!

