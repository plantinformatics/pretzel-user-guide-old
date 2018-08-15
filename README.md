# plantinformatics.io / Pretzel User Guide

This document is intended as a user manual for the plantinformatics.io instance of Pretzel.

## Accessing the site

### Registering an account

Users wishing to register on plantinformatics.io can apply for an account using the **Sign Up** tab on the landing page, or navigate directly to plantinformatics.io/signup.

![signup](https://user-images.githubusercontent.com/20571319/44134336-d2dca14a-a0a7-11e8-9a9c-53111690f206.png)

Once an email address and password has been entered, click **Submit**. Once the account has been approved by an administrator, you will be able to log in to the site.

### Logging in

Once your account has been approved, you can log in by clicking the **Log In** tab or navigating to plantinformatics.io/login. Use the email address and password you used when signing up.

## Using Map Viewer

Map Viewer allows alignment of genetic maps, physical maps, and any other linearly-represented data. Pretzel is pre-loaded with public data relevant to wheat pre-breeding research.

### Selecting a dataset

The list of available *datasets* can be viewed under the **Explorer** tab in Map Viewer. Clicking on a *dataset* name displays metadata associated with the *dataset* in the right-hand panel.

Clicking the **+** button to the left of the dataset name in Explorer will list the *blocks* available for that *dataset*. Usually, *blocks* represent chromosomes, but can also be linkage groups in a genetic map.

Clicking the **+** to the left of a *block* name in Explorer will load the data in Map Viewer.

Alignments are generated when loaded *blocks* share *features* - lines will be drawn between *features* of the same name.

#### Aligning genetic maps

Select the first genetic map you want to align. For example, we will load chromosome 2B of the `Avalon_x_Cadenza` genetic map.

![loadGenetic1](https://user-images.githubusercontent.com/20571319/44134093-8e73bcec-a0a6-11e8-99ae-218caf1df845.png)

Then select another genetic map chromosome to align. Note that you can select any chromosome, not necessarily the same chromosome as has already been loaded, but the number of features may not be high. Here we will load chromosome 2B of the `Doumai_x_Shi4185` genetic map.

![loadGenetic2](https://user-images.githubusercontent.com/20571319/44134094-91ee8d48-a0a6-11e8-971f-d9bdef3f157a.png)

Green lines are drawn between features (in this case, marker names) in common between the two maps.
