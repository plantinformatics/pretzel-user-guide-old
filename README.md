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

### Selecting a *dataset* and *block*

Available data in Pretzel is organised into *datasets* which contain one or more *blocks*. In most cases, the *dataset* is some genome-scale data, such as a genetic map or physical map, and the *blocks* will correspond to linkage groups or chromosomes.

The list of available *datasets* can be viewed under the **Explorer** tab in Map Viewer. Clicking on a *dataset* name displays metadata associated with the *dataset* in the right-hand panel.

Clicking the **+** button to the left of the dataset name in Explorer will list the *blocks* available for that *dataset*. Usually, *blocks* represent chromosomes, but can also be linkage groups in a genetic map.

Clicking the **+** to the left of a *block* name in Explorer will load the data in Map Viewer.

Alignments are generated when loaded *blocks* share *features* - lines will be drawn between *features* of the same name.

### Deleting a loaded *block*

Moving the cursor over the axis title will bring up a menu. Clicking the *X* will delete the map.

![deleteblock](https://user-images.githubusercontent.com/20571319/44135918-3e61b954-a0ae-11e8-933b-83f2c5f13f37.png)

### Aligning genetic maps

Select the first genetic map you want to align. For example, we will load chromosome 2B of the `Avalon_x_Cadenza` genetic map.

![loadGenetic1](https://user-images.githubusercontent.com/20571319/44134093-8e73bcec-a0a6-11e8-99ae-218caf1df845.png)

Then select another genetic map chromosome to align. Note that you can select any chromosome, not necessarily the same chromosome as has already been loaded, but the number of features may not be high. Here we will load chromosome 2B of the `Doumai_x_Shi4185` genetic map.

![loadGenetic2](https://user-images.githubusercontent.com/20571319/44134094-91ee8d48-a0a6-11e8-971f-d9bdef3f157a.png)

Green lines are drawn between features (in this case, marker names) in common between the two maps.

### Inverting genetic maps

It is common for genetic map linkage groups to be inverted relative to conventional short arm to long arm order.

![invertedmap1](https://user-images.githubusercontent.com/20571319/44134985-712a28f2-a0aa-11e8-882f-2504057ee7e3.png)

Moving the cursor over the axis title will bring up a menu. Clicking the *up/down* arrow will invert the map.

![invertedmap2](https://user-images.githubusercontent.com/20571319/44134984-70c4cf48-a0aa-11e8-9a08-e97a4871f547.png)

### Dragging maps

Moving the cursor over any axis tick text, the cursor icon will change to indicate the axis can be dragged and moved.

#### Re-ordering axes

The order of axes can be re-arranged by dragging maps around.

![dragmap1](https://user-images.githubusercontent.com/20571319/44136608-c187fe68-a0b0-11e8-9008-7f082c305590.gif)

#### Stacking axes

When dragging an axis, *drop-zones* denoted by light blue squares at the top and bottom of other loaded axes will become highlighted. Dragging the axis to one of these *drop-zones* will *stack* the axes on top of each other.

This is particularly useful when loading genetic maps which have multiple linkage groups per chromosome, such as the following example.

![stackmap](https://user-images.githubusercontent.com/20571319/44179887-cdf07e00-a13c-11e8-9a92-eafd43797a3e.gif)
