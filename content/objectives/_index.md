+++
title = "Project Objectives"
page = "objectives"
+++
<div class="page-header">
    <h1>Project Objectives</h1>
</div>
<div class="row text-justify">
    <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
        <p>
        Recent medical research indicates that personalized medicine approaches are paramount for addressing the problems
        related to COPD cases. In this context, mobile phone and Internet-ofThings (IOT) solutions are proven to be very
        useful. Indeed, several such mobile/IoT solutions have been investigated, by assessing their effectiveness for 
        COPD management; these systems are merely monitoring physiological signals, to provide therapeutic feedback to medical doctors. 
        </p>
        <br>
        <p>
        Another view on personalized COPD care consists of predicting disease severity based on simple clinical and 
        anthropometric data that can be introduced by individuals without medical training: age, body-mass index, 
        smoker status, etc. Consequently, medical doctors proposed two questionnaires that can be used to predict the 
        COPD stage, namely COPD Assessment Score (CAT) and Medical Research Council Breathlessness Scale (MRC). 
        Such questionnaire approaches rely on clustering patients according to relevant clinical signs. 
        Following this trend, COPD patient and disease clustering methods are also approached with the new network science. 
        </p>
        <br>
        <p>
        To achieve the main goals of our project, namely the prediction of COPD stages, efficient patient management, 
        and uncovering relevant feedback from physiological signals for medical purposes, we introduce the following 
        objectives (see the overview in Figures 1 and 2): 
        </p>
        <br> 
        <p>
        <b>O1:</b> To build a mobile application for integrating physiological signals (i.e. breathing rate, spirometry, pulse 
        oximetry, heart rate, electroencephalogram) that are gathered with a sensor network and transmitted via Bluetooth,
        with anthropometric (age, gender, Body Mass Index-BMI) and clinical parameters (comorbidities, medication, smoking
        status, COPD onset, number of exacerbations, CAT and MRC questionnaire results), which are collected by a mobile
        application. The mobile device extracts the multifractal spectra of collected physiological signals. 
        </p>
        <br>
        <p>
        <b>O2:</b> To send the smartphone-integrated data over the cloud, in order to build a COPD database and a complex 
        network model at server-level. The network model clusters COPD patients in order to find new pathophysiological
        mechanisms, leading to COPD stage prediction. 
        </p>
        <br>
        <p>
        <b>O3:</b> To build a complex network model for clustering COPD patients in order to predict the disease evolution 
        trajectory for individuals that were already diagnosed with COPD. The result consists of predicting exacerbations
        and issuing alerts when physiological signals degrade. 
        </p>
    </div>
    <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
    <figure>
    {{< img class="img-responsive" src="/images/home2.png" alt="Photo of Iovanovici" >}}
    <figcaption>Figure 1. Overview of INCEPTION at individual-level. Physiological signals are gathered with a sensor
    network and transmitted via Bluetooth. Anthropometric and clinical parameters are recorded and integrated at
    smartphone-level and then sent over the cloud in a centralized database.</figcaption>
    <figure>
    <br />
    <figure>
    {{< img class="img-responsive" src="/images/home1.png" alt="Photo of Iovanovici" >}}
    <figcaption>Figure 2. Overview of INCEPTION at server-level. Integrated individual data are collected from many 
    individuals and stored in a centralized database. The gathered dataset is then processed according to the complex
    network paradigm, in order to find new pathophysiological correlations.</figcaption>
    <figure>
    </div>
</div>