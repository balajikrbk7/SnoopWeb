# Snoop Deep Web

Resources on internet as we see can be classified into `Surface Web`, `Deep Web`, and `Dark Web`. `Surface Web` is the tip of the resources which is accessible to simple crawlers. Here with `Snoop Deep Web` we are trying to solve the problem of [Deep web crawling](https://link.springer.com/article/10.1007/s11280-018-0602-1) which is usually hidden from the reaches of simple web crawlers.

## Test Description

We want `Snoop Deep Web` to crawl a website and get its `html` and `screenshot` using [stormcrawler](https://stormcrawler.net) running in [local mode](https://storm.apache.org/releases/current/Local-mode.html) in [Apache Storm](https://storm.apache.org/). We will be providing you with instructions on the working tech stack, datasets, expected outcome and results.

### Tech Stack

- Stromcrawler
- Selenium
- Apache Storm
- Any Backend of your choice

### Datasets

[seed_urls.json](./dataset/seed_urls.json) contains list of seed domains which are required to be crawled.

### Expected outcome for 'Snoop Deep Web'

- Run [stormcrawler](https://stormcrawler.net) in [local mode](https://storm.apache.org/releases/current/Local-mode.html) in [Apache Storm](https://storm.apache.org/)
- Extract HTML data from websites in [seed_urls.json](./dataset/seed_urls.json) and store in database using stormcrawler.
- Extract Image of the complete 1080p viewport (full screen) webpage from websites in [seed_urls.json](./dataset/seed_urls.json) and store in database in [base64](https://en.wikipedia.org/wiki/Base64) using stormcrawler.

### [result.json](./output/result.json) contains a sample result with following schema

```json
{
  "seed_url": "url provided to the crawler",
  "current_url": "current url visited by crawler",
  "html": "html source code of current url",
  "base64_image": "image of the complete 1080p viewport (full screen) webpage in base64"
}
```

## Submission Checklist

Once you have completed the test successfully you are expected to provide following:

- Git repository and working code (live demo link/recorded video steps to run service)
  - Deployment steps for all the services, servers and databases
  - You can fork this repository and share the Merge Request for submission
- Share README.md, DEPLOYMENT.md, etc
  - Mention of documentation/ references/ tutorials followed
  - Clearly documenting steps to deploy and use the service
- Add in detail about one key takeaway or a new skill you picked from this exercise, providing references to articles, tutorials, examples, etc.

## Resources

| Resource     | Link                      |
| ------------ | ------------------------- |
| Stormcrawler | https://stormcrawler.net/ |
| Apache Storm | https://storm.apache.org/ |

You can find [base64_to_png.py](./utils/base64_to_png.py) utility function to check you base64 encoded image string. A sample image output is provided from execution below.
![output.png](./utils/output.png)
