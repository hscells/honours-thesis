# Semester 1

## Week 1
Started reading and collecting some interesting papers. Made a folder on Google drive to keep everything in place.

## Week 2

## Week 3

## Week 4

Did some mind mapping, which was a little helpful I guess. I went to some session that taught people how to search and I thought this was a little ironic. It wasn't very useful. I'll still stick to Google Scholar. 

## Week 5
Read a whole bunch of papers over the weekend, including a really lengthy (literature review?) about lifelogging. Made a ton of notes and organised them all into a file in google drive. I didn't realise how many ethical problems exist in this area, and I need to look more into this. Maybe there should be a section in my literature review about ethics, or possibly this should go in the project proposal.

## Week 6
After some serious writing, I got some of my friends to take a look at what I had for my literature review. Most of the comments were good, but a little unhelpful. I also got some peers to take a read, but again the feedback was pretty unhelpful. I took an in depth look into the methods for annotating images. I collected the most common techniques and also a lesser known annotation technique. The literature identified tagging, browsing and textual descriptions and my supervisor pointed me towards reverse query annotations.

## Week 7
Got my lit review reviewed by Konstantin and some peers. The notes from that include maybe talking a little bit about psych papers with relation to modelling human memory, talking about some common models for modelling human memory, talking about exactly what retrieval models exist, expanding more on the annotation and retrieval models sections and adding some images and diagrams for getting my thoughts across. I started to tackle some of these, I added some images and diagrams and I expanded a little bit more on the retrieval models section. I need to ask Guido if I can cite the research we've already done, and if this should be noted in the introduction. I still haven't written all that much on my project proposal but I'm not too concerned about it. The literature review is really taking up the majority of my reading and writing time right now.

## Week 8
Writing Writing Reading

## Week 9
Guido reviewed my lit review and I worked some more on it. The general feedback was tell and not show and to think more critically. Someone on Facebook scared every single person in the group by saying this week was submission week (phew). Developed my research questions, I am going to investigate two areas: evaluating lifelog image annotations and investigating the different types of lifelog image annotations. We also agreed that the scope of the project should be more narrow, so that rather than develop a search engine, I should just look at the annotation side of things. I will look at developing a collection of lifelog annotations to go with the collection of lifelog images.

## Week 10
More feedback from Guido, probably spent a little too much time procrastinating the day after I got my feedback but I have the rest of the week so it's fine. I need to start writing my project proposal soon. Some more writing, read some things on topic modelling but I really have no idea what I'm reading. I don't think I have a good enough background to really understand it.

## Week 11
Turns out I didn't need to read all about topic modelling in the end, just the way it's evaluated. Which is nice. I managed to get my literature review submitted and I'm pretty happy with it in the end. A lot of my peers say theirs was a lot longer than mine so that concerns me a bit. I have the opportunity to visit the NTCIR conference in Japan.. And I was accepted to go! I received funding from QUT and the NTCIR conference coordinators. I am going to present the work I have already done in the form of a poster presentation.

## Week 12
After a little bit of work on my project proposal earlier, I continued to work on it and got most of it done, with just a few minor things to fix up. Actually, a major part that I need to do it ethics as I have no idea what to write about there. I should look at some other examples of project proposals... Off to Japan! I prepared a poster and a some notes for a speech to give when I present it. I also collated some notes for when I attend the workshop on lifelogging.

## Week 13
Week in Japan for NTCIR conference, needless to say I did no work on the project proposal. Hooray for extensions! My poster presentation went really well, people were very interested in the work I was doing and during the workshop I think I made some good points. The task coordinators agreed with my comments and agreed to apply some of the them to the next round.

## Week 14
Submitted everything and gave a presentation which went very well!

# Semester 2

## Week 1
Over the break I had started to write my thesis and in the first week all I really did was keep writing. I also cleaned up the image annotation interfaces a bit. I met with Guido this week to discuss what I would be doing for the next week to plan everything out. This gave me a good starting point to go from for the weeks ahead.

## Week 2
This week I improved the usability of the image annotation interfaces and got them ready for use. This week Guido and I decided to meet every Monday to discuss my progress so far and what to do in the week to come. Guido also mentioned that he had found a masters student to perform the majority of the annotations for me - which is great since now I have to do significantly less work here and I can focus on more important things! :) I wanted to learn more about evaluation of test collections and pooling so Guido gave me a book to read.

## Week 3
After reading the chapters Guido said were most important from the book he gave me, I created a project to do trec style runs. This set of scripts to do with evaluation allows me to embed the evaluation of the annotations within a search task, which will let me know which methodology performs the best in a search task! (The code repository is located here: https://github.com/hscells/lifelog-eval) I also wrote plenty of documentation for the eval code, and for some existing image sampling code (https://github.com/hscells/lifelog-sampling). Finally, I was able to do some writing about the evaluation stuff that I had been reading about, and to write about my methodology, since it was pretty much implemented. (By the way I should mention that I had such trouble with the eval code, the elasticsearch Java APIs are very poorly documented :()

## Week 4
This week was a writing week, I wrote about the different methodologies: the efficiency at which they are collected, the performance in a search task and the usefulness of each for classifying images. This leads me to the next thing I did this week: writing a pipeline for classifying and automatically labelling images! I used some code (https://github.com/karpathy/neuraltalk2) that someone else had written which does all of the difficult stuff and I made it applicable to my lifelog images with the use of several scripts. I set up yet another repository for this code (located here https://github.com/hscells/lifelog-classification). I did some initial testing using the 100 or so textual annotations that I collected manually and the performance was pretty bad## but I suspect with many many more, it will do better.

## Week 5
After my weekly meeting with Guido, he mentioned some topics that I should investigate and write about here: TBIR and CBIR. These are two different methodologies for //image// retrieval (__text__ based image retrieval & __content__ based image retrieval). I spent some time writing about this. The master's student annotating images for me wanted a way to see her statistics (how many images she has annotated so far, the time taken to annotate, etc) so I did some work implementing this feature in the image annotation interface.

## Week 6
This week I did a lot of development work. I added a starttime and endtime to the annotation interfaces to measure how long it takes to annotate images. I also modified the interfaces so that it only displays one image at a time. It was at this point that I set up a pipeline for the automatic captioning of my images as well (this repository was renamed to https://github.com/hscells/lifelog-caption). Some initial testing of the pipeline showed some really poor results. I will need to investigate this further. I also modified how images get selected for annotation. Images that are annotated in the textual interface are now the only images that can be annotated for the other three interfaces. This is because we want images to be totally annotated for a all types of annotations (when we do evaluation). I also added a view to the image interface to display the statistics for a person's annotations. It shows the total number of images annotated for each interface, the average time and the total time.

## Week 7
I have been working on the caption pipeline and am becoming increasingly frustrated with it. It is captioning all of my images with the exact same caption. I have commented on an issue on the projects page asking about this and am yet to hear a reply. I did some more work on the evaluation code to get a more solid pipeline built. I also fixed some bugs in a variety of projects. I wrote a lot of documentation for my projects this week also. I have been doing some writing this week as well.  I didn't get much done this week as I'd hoped (creating content for databases tutorial)

## Week 8
My automatic captioning pipeline is **still** not working. I have not gotten a reply from the author on the issue and I have tried many different configurations of the tool to try to get a different result. The annoying thing is that it takes several days of training before a useful result is produced. The images are still being captioned with the same caption. Very annoying. I am considering moving away from it and trying a different tool, but most other tools are very poorly documented. I have even tried to use the pretrained model provided by the author but I am having difficulty loading it. Moving forward, I need to start thinking about how the concepts are going to be selected for the relevance assessments now (since I have enough annotations in the other interfaces). I didn't get much done this week as I'd hoped (creating content for databases tutorial)

## Week 9
I have a break through! I ended up reinstalling the tools used by the captioning tool using a different and more up to date method of installation. This has fixed everything! I can now automatically caption images using both the pre trained model and my own annotations! :). The pretrained model performs badly (as expected) and my initial testing (after a few days of training on a limited number of annotations) provides a hopeful future. I have decided, with the help of Guido, to sample 30 (at max) images from the qrels to get only the relevant images. I have done a little bit of work on the evaluation code but I am getting a score of 0 for everything (not sure why). I did some writing this week on notes for the results and discussion section of my thesis. I didn't get much done this week as I'd hoped (marking database assignments)

## Mid-Semester break
This week I implemented the code to sample the relevant images from the qrel file and upload them to the database. I spend many many hours after that annotating these images. Unfortunately my evaluation code, while retrieving images for topics, is still giving me a score of 0. Haha. After talking to Guido about this problem he found the problem. The Id's in the qrel are different to the Id's I'm using for the images. Quickly editing these values gives me some results! Hooray! I just spent the whole weekend and much of my Friday annotating images and I an getting an excellent score (obviously)! I can't wait to see how the textual annotations compare to the other annotation methodologies. I think I also would like to write a little search engine interface to demo my stuff. This all comes next week :phew:. (Also I submitted my PhD application this week!)

## Week 10
Just had my weekly meeting with Guido. This week I'll be working on doing some more writing and writing some small scripts that generate latex tables for my results section. After some tweaking, I got the latex tables to be produced every time I run an experiment which is super nice. In the same space of time I also added some code to the script to generate a table which summarises the annotation statistics (total count, total time, average time for each annotation type). This week I also generated data for a submission to ADCS; in the process I found some bugs in my code when I'm doing evaluation so it was good to catch these before they crop up when it comes around to running it for my thesis!

## Week 11
I spent this week doing writing and making amendments to my thesis. There was a lot of time spent in this week annotating images. I was able to get all of the textual annotations completed during this week which is a big boost to my morale. Other assignments are starting to creep in but it's fine.

## Week 12
