## MiniConf
BayLearn - Machine Learning Symposium.

## Links
Demo system: <a href='http://www.mini-conf.org'> http://www.mini-conf.org</a>

Source Code: <a href='https://github.com/Mini-Conf/Mini-Conf'> https://github.com/Mini-Conf/Mini-Conf</a>

## Get Started

<pre>
> pip install -r requirements.txt
> make run
</pre>

## Deploy
When you are ready to deploy run `make freeze` to get a static version of the site in the `build` folder.
Then run `make deploy` to commit and deploy the latest static site


### Tour

The <a href="https://github.com/Mini-Conf/Mini-Conf">MiniConf</a> repo:

1) *Datastore* <a href="https://github.com/Mini-Conf/Mini-Conf/tree/master/sitedata">`sitedata/`</a>

Collection of CSV files representing the papers, speakers, workshops, and other important information for the conference.

2) *Routing* <a href="https://github.com/Mini-Conf/Mini-Conf/tree/master/main.py">`main.py`</a>

One file flask-server handles simple data preprocessing and site navigation.

3) *Templates* <a href="https://github.com/Mini-Conf/Mini-Conf/tree/master/templates">`templates/`</a>

Contains all the pages for the site. See `base.html` for the master page and `components.html` for core components.

4) *Frontend* <a href="https://github.com/Mini-Conf/Mini-Conf/tree/master/static">`static/`</a>

Contains frontend components like the default css, images, and javascript libs.

5) *Scripts* <a href="https://github.com/Mini-Conf/Mini-Conf/tree/master/scripts">`scripts/`</a>

Contains additional preprocessing to add visualizations, recommendations, schedules to the conference.

6) For importing calendars as schedule see [scripts/README_Schedule.md](https://github.com/Mini-Conf/Mini-Conf/blob/master/scripts/README_Schedule.md)

### Extensions

MiniConf is designed to be a completely static solution. However it is designed to integrate well with dynamic third-party solutions. We directly support the following providers:

* Rocket.Chat: The `chat/` directory contains descriptions for setting up a hosted Rocket.Chat instance and for embedding chat rooms on individual paper pages. You can either buy a hosted setting from Rocket.chat or we include instructions for running your own scalable instance through sloppy.io.

* Auth0 : The code can integrate through Auth0.com to provide both page login (through javascript gating) and OAuth SSO with Rocket Chat. The documentation on Auth0 is very easy to follow, you simply need to create an Application for both the MiniConf site and the Rocket.Chat server. You then enter in the Client keys to the appropriate configs.

* SlidesLive: It is easy to embedded any video provider -> YouTube, Vimeo, etc. However we have had great experience with SlidesLive and recommend them as a host. We include a slideslive example on the main page.

* PDF.js: For conferences that use posters it is easy to include an embedded pdf on poster pages. An example is given.


### Acknowledgements

MiniConf was built by [Hendrik Strobelt](http://twitter.com/hen_str) and [Sasha Rush](http://twitter.com/srush_nlp).

Thanks to Darren Nelson for the original design sketches. Shakir Mohamed, Martha White, Kyunghyun Cho, Lee Campbell, and Adam White for planning and feedback. Hao Fang, Junaid Rahim, Jake Tae, Yasser Souri, Soumya Chatterjee, and Ankshita Gupta for contributions.

### Citation
Feel free to cite MiniConf:
```bibtex
@misc{RushStrobelt2020,
    title={MiniConf -- A Virtual Conference Framework},
    author={Alexander M. Rush and Hendrik Strobelt},
    year={2020},
    eprint={2007.12238},
    archivePrefix={arXiv},
    primaryClass={cs.HC}
}
```
