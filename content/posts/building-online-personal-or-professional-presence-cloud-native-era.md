---
title: "Building an online Personal / Professional presence in the Cloud (Native) Era"
description: An article about my recent experience on establishing an Online Presence in the Cloud Native Era
date: 2021-08-14T22:43:26+03:00
publishDate: 2021-08-14T22:44:26+03:00
draft: false
---
{{<figure src="/posts/images/online-presence-in-the-cloud-era-presence-800px.jpg" caption="Photo by [eberhard 🖐 grossgasteiger](https://unsplash.com/@eberhardgross?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/photos/_uAVHAMjGYA?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)" link="/posts/building-online-personal-or-professional-presence-cloud-native-era/#content">}}

This article is intended to share my perspective and recent experience on establishing an online (Content Management-focused) presence for any individual (or small Team) that wants to create content online, whether at a Personal or Professional level, with the wishes that it will prove useful as a starting point. Your context, technical savviness and goals will dictate how complex things will get upon embarking on this journey.

<!--more-->

I will try to keep things as general as possible, with the hopes that this text will *stand the test of time*, only later on being specific with examples as to put some practice behind the upcoming shared experience. A fair majority of examples will be related to Amazon's AWS Cloud (as this is where the server and setup behind this article is hosted), but the general principles can be transported/reused in a Cloud agnostic manner, with one having to adjust to a specific Cloud Service Provider's (CSP) lingo or Services Offering. More on this below.

:information_source: *Disclaimer: I have no affiliation with Amazon AWS, Microsoft Azure or Google Cloud Platform and this article is in no way intended as advertising towards any of them. However, do note that links may include Referral IDs such as to help, perhaps, keep Hosting Costs down for the resources you find on this website.*

### Considerations

In the following sections, a few thoughts will follow about:

- why use a Cloud versus On-premises setup to begin with;
- what Content Management strategies could one adopt in the Cloud;
- a perspective on choosing between the different Cloud Service Providers, and
- about Costs and their Optimization

So...

#### Why use the Cloud and not go for a more traditional On-premises approach?

Many years back, if one wanted to setup an online virtual space for their Web Application or Product they would have just a few options:

- for simple setups such as Websites (think Marketing Landing Zones, Portfolios, Blogs etc.) they could go with a Hosting Provider that offered a (Hosting) Package for the Physical Servers that were needed. Back then, there were no Virtual Machines but actual Hardware sitting in a rack, in a Datacenter somewhere. Costs would be covered based on a Subscription model (Monthly or Yearly) with the Server Infrastructure arriving in a fixed configuration. One was essentially renting out the Server Hardware.
- for more complicated setups (imagine a Front Office and Back Office e-Commerce setup, or an Online Gaming service made from both Frontend and Backend infrastructure) this was really hard to achieve with a simple Hosting Provider. How fast could they ramp-up new Servers? Who would secure the Data? As such, most big Companies adopted a On-premises setup with them investing/buying all the needed Servers, Storage, Network and Infrastructure Management software and after tweak that to host and scale based on demand. Running at scale meant they would have dedicated Teams of Infrastructure Engineers (System Administrators, Database Administrators and Network Administrators) on top of the main Programming Teams in charge of creating the actual Code delivering the Experience or Service as intended. Countless Hours and dedicated Human Resources would go into Developing (Features, Components) or any required Networking, Security and Managing (OS, Software and Security Patching etc.) followed by Deployment. Sounds complicated, right?

With the arrival of Cloud-hosted Technology, everything changed. Here is an attempt at a simple explanation: new entities called Cloud Service Providers (CSP) joined the mix of traditional Hosting (Service) Providers; these would go on develop and promote the *Shared Responsibility Model* (see Figure 1. below) -- a set of principles and practices -- which entails that most of the (Server-related) Resources and Costs associated with Infrastructure Management on your side (the "Customer") would be considerably lower compared with similar classical On-premises setups. In short, the CSP would take care of setting up most the Infrastructure (Infrastructure-as-a-Service/IaaS) and Platform (Platform-as-a-Service/PaaS) needs that you require, covering Updating, Patching and some Security, while in turn allowing you (your Team or your Business) to focus only on Feature or Component Development *and* Delivery of your Product to your audience. Almost every aspect of your Server and Network Infrastructure requirements is taken care of *in the Cloud*, by the Vendor. This is called a Managed Services approach and it is one of the selling points of Cloud, due to the lesser Time-to-Market (minutes/hours instead of months) for a modern Online-first Software Product. Welcome to the Cloud (Native) Era!


{{<figure src="/posts/images/SRM-Division-of-Responsibilities-1-1024x632.jpg" caption="Figure 1. A Vendor-agnostic view of the Cloud Shared Responsibility Model, from [Cloud Passage](https://www.cloudpassage.com/articles/shared-responsibility-model-explained/)">}}
​     

While all of this sounds easier, there are caveats. After Cloud adoption, one would have extra things to figure out; as an example, covering various Compliance and Audit needs when it comes to Data Management and Privacy -- as today the most valuable digital resource of an Internet-first Company is actually the Data engulfed and not the Servers and Software providing the experience. This subject is worth a wider discussion outside the scope of our current endeavor, thus I shall not add more on it right now.

Safe to say, yes, Cloud is more feasible from an Infrastructure Management and Costs perspective for most needs, compared to more traditional setups, but with its own hurdles. Okay, enough for now, time to focus on Content!

#### Choosing a Content Management strategy

For the scope of this article, we will be focusing on basic (static) Content Hosting and Management as i.) it is more simple to detail, and ii.) focuses on the reader achieving a similar goal to creating the experience that you have in front of you, facilitating the hosting of these words. If time will ever allow, I will add thoughts for more complex setups such as Front Office/Back Office or Frontend and Backend architectures.

Web Content usually takes two implementation approaches: *static* and *dynamic* management of the content intended to be presented.

**Static Management.** This means that everything (such as this Post's text and images), an Image or Photos Catalog or similar resource is (mostly) static, everything being categorized as objects to be shown (rendered) via a User's Browser and intended for minimal interaction. The Data barely changes over time.

Implementing a Static Management strategy usually entails using a simple generator software (which may be free of Costs), such as [Jekyll](jekyllrb.com/), [Hugo](https://gohugo.io/) or even a custom/tailored one created for your (Business') needs via classic HTML & CSS approach --  this usually provided by a Digital Marketing Agency (which may entail some extra Costs).

**Dynamic Management.** For this category, the content changes more over time or frequently, usually based on User input. For example, a Recommendation Engine that allows Online Shoppers to decide between similar Products may adjust recommendations based on their Ratings, with the presentational content (Product Specifications and Description) accompanying them.
Catering to implementing a Dynamic strategic may include, at Individual-level, software such as [WordPress](https://wordpress.com), SMB-level,  [PrestaShop](http://www.prestashop.com/en/) and Enterprise-level [Adobe Experience Manager](https://business.adobe.com/products/experience-manager/adobe-experience-manager.html).

The Static strategy is intended for simple use cases, requiring little User input and small-to-no integration with other 3rd Party Software and Systems, whereas the Dynamic strategy is suited for more advanced setups and use cases where User input and 3rd party Systems reliance takes priority.

In fact, this very Post is actually static content generated with Hugo from Markdown, and a visually customized [Personal Web](https://themes.gohugo.io/themes/personal-web/) Theme, as my needs are only to present you with text and some images in a pleasant to use layout. No fancy setup such as User Registration, Commenting or Database is needed, as most of these things can be covered in other ways. The continuation of this article assumes that your intention is to start with a similar Static Content Management approach.

#### Deciding between modern Cloud Service Providers

If one were to look nowadays for Cloud Service Providers they would be somewhat lost at first, perhaps stuck somewhat deciding between all of them. The marketplace is [led by giants such as Amazon AWS, Microsoft Azure, Google Cloud Platform and Alibaba Cloud](https://www.statista.com/chart/18819/worldwide-market-share-of-leading-cloud-infrastructure-service-providers/) (see Figure 2. below, for a breakdown).


{{<figure src="/posts/images/market-share-of-csp.jpeg" caption="Figure 2. Cloud Service Providers (CSP) Infrastructure Market Share in Q1 2021, from [Statista](https://www.statista.com/chart/18819/worldwide-market-share-of-leading-cloud-infrastructure-service-providers/)">}}  


With so many Providers and Service Offerings it may be overwhelming to dive in anything, at first. What criteria should go into your consideration? Should it be actual Vendors, Services types, Costs or Customer/Developer Experience?

Based on my [Professional Experience](https://www.bogste.ro/about/) to date, I will try to keep things simple and suggest you go on the following path:

- if you are an **Individual or small Team** or just starting out, choose between any one of the Top 5 CSP Market Leaders above, as the Knowledge available about setting-up and troubleshooting things inside their Cloud is more widespread and accessible, for each. At the same time, if you or your Team Members are already versed in the Technology Stack of any of them that may weigh in your decision more, thus factor that in also.
- if you intend to bring your **Small-to-Medium Business (SMB)** into the Cloud Journey, start with the above consideration and include an initial Pricing/Costs Calculation as a deciding factor between all of the CSP and your Budgetary needs. Try an estimation using [AWS](https://calculator.aws/#/)', [Azure](https://azure.microsoft.com/en-us/pricing/calculator/)'s, [Google Cloud Platform](https://cloud.google.com/products/calculator)'s or [Alibaba Cloud](https://www.alibabacloud.com/pricing-calculator#/)'s Pricing Calculators (as purely examples, listed in order of Market Share above) over a period of 3-to-5 years.
- if you are an **Enterprise**, and planning on building a more complex Online Application, take into account all above plus any legal or your own Company's constraints on Data Privacy and Compliance (i.e. such as Europe's GDPR,  your internal regulations or your National Administration's laws). These may require you to keep the Data only in European Data Centers or On-premises. Moreover, if you have specific Service Level Agreements (SLA) demands, it is worth noting that these differ from one CSP to another.
- in **general**, technologically all CSP follow similar Architectural Principles and their Services Offerings do not differ by much. Each uses their own Marketing/wording for similar underlying technologies. Take [Kubernetes](https://kubernetes.io), for example: Amazon calls it [EKS (Elastic Kubernetes Services)](https://aws.amazon.com/eks/), Azure names it [AKS (Azure Kubernetes Services)](https://azure.microsoft.com/en-us/services/kubernetes-service/) and finally Google brands it as [GKE (Google Kubernetes Engine)](https://cloud.google.com/kubernetes-engine). Under-the-hood it is still Kubernetes, but running in a *Managed Services* context, and thus if you or Software Engineers in your Team(s) know how to use it you/they will be able to do so with regardless of the overhead of the CSP's own underlying sugarcoating.

For this Website, my needs fall mostly into the first point above, and thus I have chosen Amazon AWS.

As a quick recap on my decisions, until now, I have chosen Hugo as my *Content Management System/Framework* (given that the Learning Curve was minimal-to-moderate for me) and *Amazon AWS* as the Cloud Services (Hosting) Provider (as it is the most "popular", with lots of technical knowledge available in the related [StackOverflow tags](http://stackoverflow.com/questions/tagged/aws) or [AWS Community](https://aws.amazon.com/developer/community/)). *Pricing* did not account for much in my decision making (more on this later, but suffice to say), because almost if not all of the CSP mentioned until now offer what is called a *Free Tier*; and if my actual *"Cloud Usage"* patterns, as measured across the days/months, fall under a certain threshold level I will be eligible to very little to no costs at all. However, the only cost worth mentioning on my end was the actual Time spent and Complexity encountered while setting everything up, a consideration which leads us to our next section...

#### Picking the right Service Offering for the job from a chosen CSP

Building out your Solution for your Product and related Performance Requirements comes down to a single need: how much control of your underlying Infrastructure do you require?

This need of Control is important, as based on it you will have to choose between a fully Managed deployment model (less Control for the Customer, with the CSP covering all Infrastructure setup in your behalf) or an Unmanaged model  (most Control is deferred to the Customer) offering better evolution. Let us see.

For a Website such as this one for which my intention is to host articles, my Resume and details on my Projects and Hobbies (so, fairly basic needs to build for to begin with) a typical course is accounting for:

1. in an Unmanaged scenario I will need a basic Web Server and Storage setup, in the Cloud. For my choice of AWS Cloud, this could mean that the Servers can be deployed and ran in a couple of [AWS Compute](https://aws.amazon.com/products/compute/)'s *EC2 (Elastic Compute Cloud) Instance(s)*. These are Amazon's equivalent of *Virtual Machines/VM*, which will be hosting the actual textual content; and any assets (images and documents) would be stored in an Instance-attached *ECS (Elastic Compute Storage) Volume* and/or *S3 (Simple Storage Service) Bucket*. In other words, I would be using a combination of AWS' IaaS offering.
   This would allow me the most control of the whole underlying Infrastructure, if I ever decide to evolve my setup and integrate other components, such as a Database to accommodate Newsletters subscribers later on. However, as described in the *Shared Responsibility Model* above, that leaves things such as setting up Networking, Updating, Patching and Security on my plate. Of course, modern Configuration Management tools such as [Terraform](https://www.terraform.io) may help ease all the overhead thus take it into consideration, based on your needs.
2. in a middle-ground Unmanaged-to-Managed approach, for my simple needs as described previously, AWS offers the option to [transform an S3 Bucket into a Website](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html) with a somewhat simple toggle switch, under the hood, and a prerequisite setup of Network Policies. It is a simpler approach than 1), evolution being limited yet still possible to some extent.
3. aiming for a fully Managed scenario, AWS offers the [Amplify](https://aws.amazon.com/amplify/hosting/) service as a starter (PaaS) for my specific [Use Case case of hosting a Static Site](https://aws.amazon.com/getting-started/hands-on/host-static-website/) supporting Hugo Out-of-the-Box. This choice allowed me to deploy everything you see on this website and distribute it globally in under 10 minutes. Basically, I provide the content under [my GitHub Repository](https://github.com/bogste/bogste.ro) and AWS takes care of fetching it, then building, scaling and distributing it across its [Global Cloud Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/) whenever I make a change to it. Excellent!
   Since everything you see here is statically generated, once, there is no need to cater for any special Networking (i.e. setting up Routing Tables), Security (i.e. Web Application Firewall) or Updating/Patching (as Amplify always utilizes Amazon's most up-to-date and secure Images).
   The downside? On one end, I only control the content, having to rely fully on Amazon for providing the Infrastructure which may save me a lot of time but may incur more Costs down the road. We will see how things fare in the long run.
   On another end, if there will ever be a need to change my setup towards a more dynamic nature, evolution may be severely limited as every PaaS is similar to a locked and self-sustainable garden/ecosystem: everything is nice and good between its walls, but try and move something outside and it may be lost or impossible to transfer.

Again, how much Control do you need? Wishing the above three points helped point you in the right direction.

Be mindful that other CSP may provide similar Solutions, perhaps under the same *Compute* moniker and/or PaaS solutions which may easily cater to your specific/exotic needs and deployment choices. Homework will have to be done, beforehand!

One last consideration is...

#### Being mindful of Costs (as part of your Cloud Optimization strategy)

On our journey until now, I left out Costs out of the discussion because these are highly dependent on your actual Usage patterns. They may range from zero up-to a few (possibly thousand) Dollars a Month (for a heavily used Enterprise setup). The most commonly documented way of mistakenly supporting extra Costs is caused by orphaned components, idling, which use up Cloud Resources without doing any meaningful work. It is literally akin to leaving Home for a Vacation, but forgetting all the lights and appliances on only to find out that your bill has increased

For my case, AWS Cloud offers limits called [Service Quotas](https://docs.aws.amazon.com/general/latest/gr/aws-service-information.html) specific to my *Free Tier* setup after which their consumption thresholds are reached (extra) costs may apply. To make things easier, by default they offer a free service called [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/) that sends out timely Alerts whenever any limits may be reached soon (see Figure 3. below). As a more advanced alternative, one can check [Costs & Usage Reports](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/) as a way to gauge usage costs for any setup. For my case, AWS Amplify seems enough to keep everything under the price of a Coffee, per Month.


{{<figure src="/posts/images/aws-budgets-alerts.jpg" caption="Figure 3. AWS Budgets Alerting about S3 Bucket reaching Free Tier limits">}}  


In general, if you have more advanced Business Requirements be mindful to account for this as part of your Cloud Optimization strategy; you should monitor these Reports on a Monthly basis and be on the lookout for any opportunity of Costs Saving. After all, one should pay only for what they actually use.

#### Ending Thoughts

This article's purpose was to share a perspective about how one could get started setting up an Online Presence in the Cloud Native Era.

Initially, after the introduction, I shared my thoughts on choosing between a Static or Dynamic Content Management strategy, and picking Hugo as my Content Management System/Framework. Later on, I tried shedding some light about picking between the different Cloud Service Providers based on some simple considerations.
Lastly, I focused on the goal of Hosting a (Static) Website in the Cloud using AWS's Amplify PaaS, given my subjective needs, and then wrapped up with a few thoughts on Costs (as part of Cloud Optimization area).

Thanks, for lasting through to the end! Wishing you found at least some things in the above useful.

Feel free to add any Comments, Feedback or reach out to me in private, via Email for any follow-ups!

Until the next one... Cheers,

{{<figure src="/images/bogste-profile-photo-128px.png" alt="Ian Bog'Ste Profile Photo" class="rounded-img" link="/about/#content" >}}
--Ian
