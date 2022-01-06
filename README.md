rss-roller
==========

[2022/01/06] This branch is a version with my modification as below,

- Fix the full URL issue
- Support the ignored posts
- Support the posts sort by timestamp
- Minor update on the format
- Start using html-xml-utils (☛ [Don't Parse XML/HTML With Regex](https://stackoverflow.com/a/1732454/3776858))

  In this case, please have html-xml-utils installed if you would like to try this.
  
  Like on macOS, it can be installed,
  
      brew install html-xml-utils

---

Shell script for generating and updating rss feeds. 

When you first run the code it will generate a dotfile `~/.rss-roller.rc` and it will ask you some default questions for the RSS file. It is up to you how much you write in these fields but they are required to create a valid rss file. The last two questions will ask you where the RSS file should live on your disk and what the name of the rss file will be. It would be sensible to name the script with an `.xml` suffix. It will also ask where your posts live, leave this blank if do not have a dedicated folder of posts to use in auto mode.

It has two modes, an auto mode where it will go through the designated folder of posts and generate the information as needed using the following flag.

        rss-roller --auto


There is also a manual mode which is better for single page layouts, and far more robust, which will then ask you a series of questions to generate the blog. This can be summoned using

        rss-roller --manual

It is worthwhile checking that the rss feed created is valid using an [online tool](http://validator.w3.org/feed/) if the rss file generated doesn't work as expected.
