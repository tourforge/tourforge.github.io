# Building an app

Since TourForge Baseline is a Flutter library, it can be used to create a tour guide application with customized branding without code changes to the library itself. Keep in mind that branding is only one piece of the puzzle: tours themselves must be created as well.

The steps below should help give you an idea of what is required to create a tour guide app with TourForge Baseline.

1. Create a fork of the [TourForge Baseline](https://github.com/tourforge/baseline) repository and clone it to your local machine.
2. Get the app running by following the instructions in the TourForge Baseline repository's README.
3. Upload your tour content, created using [TourForge](https://github.com/tourforge/builder), to a webserver. The content with its full directory structure should be accessible via HTTPS. You will need to know the base URL of where the content is accessible, for example: `https://example.org/tour-content/`.
4. Change the URL in the `app/lib/main.dart` to whatever your content's base URL is.
5. Check and see if the app now loads your content instead of the default content. If not, here are some troubleshooting tips:
   - Is it still showing the default content? If so, you might not have changed the right URL.
   - Is the content not loading at all?
     - Check the logs to investigate the exact error.
     - Most likely, content not loading means that the URL is wrong or your webserver is not properly configured to serve the files.
     - Try manually requesting the tour data from your webserver to see if it works that way.
6. Customize the application's branding as you see fit.
