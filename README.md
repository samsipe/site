site
====

My website, [samsipe.com](https://samsipe.com), thanks for all of the help setting this up Otto. 

### To Install:

- `npm install` will install all packages.
- `bower install` will install web dependencies.

### To Run:

- `gulp serve` will open live preview in browser.

### To Edit:

- Edit the json files in `site/app/data`.
- The file `info.json` has basic site info and pages.
- All of the other json files are optional.

### To Deploy:

- Create a file called `aws.json` with your S3 keys in the root directory of the repo.

    ```
    {
        "key": "KEY",
        "secret": "SECRET",
        "bucket": "domain.com"
    }
    ```

- `gulp deploy` will deploy to AWS S3.

### To run a Browser Test:

- `gulp serve`  in one terminal window 
- `docker run --rm -v "$(pwd):/sitespeed.io" sitespeedio/sitespeed.io:15.6.4 -b chrome http://localhost:9000` in another 