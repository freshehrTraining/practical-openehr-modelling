---
hide:
  - navigation
---

# Practical openEHR modelling

## **Getting started**

1. Open a web browser – Chrome, Edge or Firefox are best

2. Go to [https://tools.openehr.org/designer](https://tools.openehr.org/designer/) 
(Best if you open this link in a new tab).


3. Login: 		`freshehr_training`	
   Password: 	`ad4freshtraining`


4. Choose the repository allocated to you
      - Gryffindor, Hufflepuff, Ravenclaw, Syltherin or Tatooine.

5. Find ‘Nursing Admission Assessment STARTER.v0' in the list of templates and click to open the template.

6. Open the original ['Nursing Admission Assessment paper form'](Nursing%20Admission%20Assessment.pdf) (Best if you open this link in a new tab). 


## **A. Tidy the basic template**

### Problem/Diagnosis	

 - Rename the Problem/Diagnosis archetype to 'Main Diagnosis'

- Constrain out everything apart from 'Problem/Diagnosis name'

### Adverse Reaction Risk

- Pull in the 'Adverse Reaction Risk' archetype

- Set it's occurrences to **0..*** to allow multiple allergies to be recorded.
  
- Constrain out everything apart from 'Substance' and 'Manifestation'

- Rename ‘Manifestation’ to ‘Reaction Details’ and make it mandatory

### Medication Order

- Clone 'Specific direction description'

- Rename one to 'Dose' and the other to 'Frequency'

### Vital Signs section

 - Pull in Pulse Oximetry into Vital Signs section

- Constrain out everything apart from 'SpO2' ratio

- Make 'systolic' and 'diastolic' Blood pressure mandatory


### Add a Clinical Frailty scale

Go to the International CKM 

[https://ckm.openehr.org/ckm/archetypes/1013.1.4691/export](https://ckm.openehr.org/ckm/archetypes/1013.1.4691/export)

 (Best if you open this link in a new tab).

- Press the ‘Export ADL’ button and save the archetype somewhere on your system

- Go back into Archetype Designer and go to top-menu->‘Import’ then either Browse to your file or drag and drop then Upload.

- Go back to your template, click on ‘content’, then pull in the Clinical Frailty scale from the list of archetypes on the right.

## **B. Create a new local archetype - Additional information on admission**

The nurses have used the templates you created but have asked for some changes.

You can view the original document here  

['Additional Information on Admission'](Additional%20information%20on%20admission.pdf) (Best if you open this link in a new tab).


- Create a new `ADMIN_ENTRY` archetype called ‘Inpatient admission details’ then add these ‘element’ datapoints ...

**Mode of access**	

		Ambulatory  	

		Wheelchair	

		Stretcher	

		Other		_________________________________

**Transported with**
		
		Oxygen	

		Monitor	

		IV		

		Other		_________________________________

**Admission method **	

		Waiting list		

		Booked		

		Planned		

		A&E department	

		General Practitioner	

		Bed Bureau	

		Consultant Clinic	

		Other			____________________________		

**Additional Help needed**	

		Yes  	     No  

Once you have created your new archetype, go back to your template. 

Highlight `content`, add your new archetype then Save the template.


## **C. Adding SNOMED CT bindings**

If you have time, try looking for [SNOMED CT] terms that match the Valuesets in'Admission method' and 'Transported with Oxygen' via the NHS SNOMED browser https://termbrowser.nhs.uk/?

This is not always easy and raises issues about correct use of SNOMED CT terms in a very specific context.

For instance there are 1649 matches for 'oxygen' - which is the correct term to use in the context of 'Transported with' ?


## **D. Additional material**

### General

**openEHR resources** 

[openEHR website](https://www.openehr.org/)

[openEHR videos and presentations](https://www.youtube.com/c/openehr/featured)

[openEHR Discourse (discussion forum)](https://discourse.openehr.org/)

[What is openEHR? - Introduction](https://www.openehr.org/about/what_is_openehr)

[openEHR Zotero library](https://www.zotero.org/libraries)


**Clinical Knowledge Managers (CKMs):**

[International CKM](https://ckm.openehr.org/ckm/)

[Apperta CKM (UK)](https://ckm.apperta.org/ckm/)

[Norwegian CKM](http://arketyper.no/ckm/)

[German Highmed CKM](https://ckm.highmed.org/ckm/#)


### **Manchester Pharmacogenetics project**

[This presentation by Jessica Keen](https://668faff97d68b98d365a.b-cdn.net/wp-content/uploads/2023/04/Jessica-Keen.pdf), Pharmacy Lead at NHS NW Genomic Service Alliance is a great overview of the project.

<img src="images/pgx-as-service.png" width="400">

[Uni Manchester Pharmacogenetics models](https://ckm.apperta.org/ckm/projects/1051.61.64)

### **Social Care project**

[Social Care Project on Apperta CKM](https://ckm.apperta.org/ckm/projects/1051.61.50()

A repository for the social care related archetypes and templates that we have been working on for various use cases
[Care Home Dataset template](https://ckm.apperta.org/ckm/templates/1051.57.273)

Based on the care home data inventory [described in a recent paper by Lucy Johnston et al](https://www.medrxiv.org/content/10.1101/2020.08.17.20176503v2) from Edinburgh Napier University.  

The original data inventory is shown below, along with another care home dataset that we have used as an example in our data models.
![](images/care-home-data-stds.png)


## This site is hosted at... 
 **`https://freshehrtraining.github.io/practical-openehr-modelling/` **

<img src="images/qrCode.png" width="150">

