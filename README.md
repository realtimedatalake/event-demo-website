# Event Demo Website
This is a simple website instrumented with [analytics-next-cc](https://github.com/realtimedatalake/analytics-next-cc) – rtdl's fork of Analytics Next (aka Analytics.js 2.0). The site has text fields, a dropdown, and a submit button that fires several events onClick. The analytics-next-cc configuration will carbon copy (cc) all events that are sent to Segment to the `ccUrl` (set to `"http://localhost:8080/ingest"` in website) option and restrict sending events to Segment depending on the `dontSendToSegment` option (set to `false` in website).

## How to Use
    1.  Update all `[your_write_key]` to your Segment write key in index.html
    2.  Update the `ccUrl` and `dontSendToSegment` options in index.html
    3.  Save index.html
    2.  run `docker run -dit --name rtdl-demo-site -p 8085:80 -v "$PWD":/usr/local/apache2/htdocs/ httpd:latest`

