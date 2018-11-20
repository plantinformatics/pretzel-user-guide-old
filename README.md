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

### Brushing maps

Moving the mouse over an axis will change the cursor to a *+* sign. Clicking and dragging up/down will create a *brush* - a selection of an interval in the axis. Any features inside the brushed region will be listed in the table of *features* in the right panel. Moving the mouse over the features in the table will highlight the feature in the axis with a yellow dot.

#### Editing the brush

Once a brush has been made, it can be moved up and down the axis, or extended in either direction.

### Zooming maps

![brushing](https://user-images.githubusercontent.com/20571319/44180317-05602a00-a13f-11e8-96b1-d9568585807a.gif)

Once a *brush* has been made, clicking the *zoom* button will *zoom* the axis to the interval defined by the *brush*.

![zoom1](https://user-images.githubusercontent.com/20571319/44180321-0a24de00-a13f-11e8-9602-0f5100b8b6b9.gif)

### Loading physical genomes

In addition to genetic maps, Pretzel is pre-loaded with the International Wheat Genome Sequencing Consortium (IWGSC) RefSeq v1.0 genome assembly pseudomolecules, with High Confidence and Low Confidence gene annotations and 90k marker positions available as *feature tracks*.

Before loading genes or marker *tracks*, the chromosome should be loaded first.

![loadphysical1](https://user-images.githubusercontent.com/20571319/44186251-a957ce80-a15b-11e8-83e5-d1bffcb75765.png)

An axis is drawn with the full length of the pseudomolecule, but no features are loaded. Users can then select which *child* datasets to load into this axis: for example, gene annotations or marker positions.

Here we load the 90k marker positions for chromosome 7A, and then select a genetic map to align.

![physicaltogenetic](https://user-images.githubusercontent.com/20571319/44186403-909be880-a15c-11e8-9b3f-f064dfce83c4.gif)


## Uploading data

Users are able to upload data by clicking the Upload tab in the left panel of Map Viewer. By default, uploaded data is accessible only to the user who uploaded it. Users are also able to make data accessible to other users (see below).

Data can be uploaded in CSV format, JSON format or cut and pasted from a spreadsheet application such as Excel.

### Uploading as CSV

Select the CSV option under Data Specification.

![image](https://user-images.githubusercontent.com/20571319/48755988-83f2d780-eceb-11e8-83a5-496425c5d9ba.png)

To upload a new dataset, select "new" under *Dataset* and enter the name of the dataset.

If the dataset is a genetic map, then *Parent* should be None. If you are defining positions inside an existing dataset, such as your own marker positions inside a genome assembly already available in Pretzel, you should select that reference genome as the *Parent*.

For example, if you are defining the location of markers in the IWGSC RefSeq v1.0 assembly, select `Triticum_aestivum_IWGSC_RefSeq_v1.0` as the parent. 

For all genetic and physical map data, type should be *linear*.

*Namespace* can be used to define a distinct set of names for a marker or gene set. This is useful for example when a set of markers includes as aliases the index position in the array, so that multiple marker sets may define a marker named "1", for example.

In particular, if you are uploading a genetic map using 90k markers, *Namespace* should be `90k`. This will take advantage of the aliases defined for 90k markers. Note that if you omit namespace in this case, only direct links will be drawn (between markers of the same exact name).

To upload the map data itself, you can either select a CSV file on your computer by clicking Choose File, or cut and paste into the table directly. Feature, Block and Position refer to marker, chromosome (or linkage group) and position.
