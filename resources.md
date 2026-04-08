---
title: Available resources and training
---

This page outlines the computational infrastructure, specialist support, and software resources available to ABLeS project teams. Quick links and how-to guides are included to help you make the most of these resources.


## 1. Computational resources

ABLeS projects may receive compute and storage allocations on both the Pawsey Supercomputing Research Centre and the National Computational Infrastructure (NCI).


<div style="display: block; margin-left: auto;  margin-right: auto;">
    <style type="text/css">
    .tg  {border-collapse:collapse;border-spacing:0;}
    .tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
    overflow:hidden;padding:10px 5px;word-break:normal;}
    .tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
    font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
    .tg .tg-ltol{background-color:#205a86;border-color:#000000;color:#ffffff;text-align:center;vertical-align:middle}
    .tg .tg-4jry{background-color:#c0c0c0;border-color:#000000;text-align:center;vertical-align:middle}
    .tg .tg-j13t{background-color:#205a86;border-color:#000000;color:#ffffff;text-align:center;vertical-align:top}
    .tg .tg-hxuv{background-color:#205a86;border-color:#000000;color:#ffffff;text-align:center;vertical-align:middle}
    .tg .tg-maf8{background-color:#656565;border-color:#000000;color:#ffffff;text-align:center;vertical-align:middle}
    .tg .tg-xwyw{border-color:#000000;text-align:center;vertical-align:middle}
    .tg .tg-yn16{background-color:#9b9b9b;border-color:#000000;color:#ffffff;text-align:center;vertical-align:middle}
    </style>
    <table class="tg">
    <thead>
    <tr style="font-weight: bold;">
        <th class="tg-xwyw" colspan="1"></th>
        <th class="tg-maf8" colspan="1">NCI</th>
        <th class="tg-maf8" colspan="1">Pawsey</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td class="tg-hxuv">Compute infrastructure</td>
        <td class="tg-xwyw" colspan="2">HPC and Cloud</td>
    </tr>
    <tr>
        <td class="tg-hxuv">Temporary storage</td>
        <td class="tg-xwyw">5 TB</td>
        <td class="tg-xwyw">1 PB</td>
    </tr>
    <tr>
        <td class="tg-hxuv">Project storage</td>
        <td class="tg-xwyw" colspan="2">5 TB</td>
    </tr>
    <tr>
        <td class="tg-hxuv">Default service units</td>
        <td class="tg-xwyw" colspan="2">50 kSUs per Quarter</td>
    </tr>
    <tr>
        <td class="tg-j13t">Specialist support</td>
        <td class="tg-xwyw" colspan="2">Yes</td>
    </tr>
    </tbody>
    </table>
</div>

**Notes:** 

- These allocations are reviewed quarterly.
- Additional resources may be granted as long as the required resources are available.
- Time frame: Software projects are limited to 6 - 12 months

{% include callout.html type="note" content="Additional resources may be requested by project leads [**using this form**](https://docs.google.com/forms/d/e/1FAIpQLSe_zrqiE7QSh1FFlmzMxFV6F_u5G-4dnAJ1H7vpN6kkkATyww/viewform?usp=header)." %}


#### About the resources available at each computational facility


##### Pawsey Supercomputing Centre

ABLeS includes 10 million service units (SUs) of compute capacity on [Setonix](https://pawsey.org.au/systems/setonix/) and flexible storage on the fast S3 based [Acacia](https://pawsey.org.au/systems/acacia/) storage system. These SUs can be utilised across CPU and GPU nodes.

Centrally installed software and popular bioinformatics reference datasets are available on Pawsey. You can find more details **[here](/ables/if89/)**.


##### National Computational Infrastructure (NCI)

ABLeS encompasses 16 million SUs of compute capacity and 500 TB of storage available per annum on the [Gadi supercomputer at the NCI](https://nci.org.au/our-systems/hpc-systems). These SUs can be utilised to run jobs on different nodes of Gadi that are equipped with either CPUs or GPUs.

{% include tiles.html type = "gadi" %}


## 2. Specialist expertise

ABLeS projects can access expert support from NCI, Pawsey, and ABLeS specialists to install, develop, optimise and deploy tools and workflows.

{% include callout.html type="note" content="If you are part of an ABLeS project and need help, please submit a request through [**this Google Form**](https://docs.google.com/forms/d/e/1FAIpQLSere1PvgPEuJkpvQUk1-11C88IAeQNQKEUFc-Qgbn5GgKK2jw/viewform?usp=sf_link)." %}


#### Pawsey training

Pawsey offers a range of in-person and online trainings, workshops, and activities to help you best use Pawsey resources.

{% include tiles.html type = "pawsey" %}


#### NCI training

NCI provides <a href="https://nci.org.au/users/user-training">training resources and in-person training courses</a> throughout the year to help develop the skills of the NCI user community.

{% include tiles.html type = "nci" %}


## 3. Software and reference data

#### Pawsey Supercomputing Centre


##### Software

There is a wide range of centrally installed software for Setonix users, including popular bioinformatics tools. More information about [software on Setonix](https://support.pawsey.org.au/documentation/display/US/Software+Stack).

Setonix users can also install their choice of software on the `/software` partition. We also encourage usage of containers with Singularity. Users are able to download any containers they like!


##### Reference datasets

Popular bioinformatics [reference datasets](https://support.pawsey.org.au/documentation/display/US/Life+Science+and+Bioinformatics) are available on Pawsey. Additional reference sets can be requested via <help@pawsey.org.au>


#### National Computational Infrastructure (NCI)


##### Centrally supported software: `/apps`

Centrally supported software available through NCI can be [**viewed here**](https://opus.nci.org.au/display/Help/5.+Software+Applications).


##### Shared repository of tools and software: `project if89`

All NCI users can also join the [**Australian BioCommons Tools and Workflows project**](resources): in project allocation `if89`. This is a repository of popular software tools, containers, and workflows that can be used by anyone in the NCI system.

Anyone from an NCI project is also invited to [**contribute to `if89`**](/if89-technical), and add more software installations that can be shared with others.



