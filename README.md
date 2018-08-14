## UCSC custom track
1. In the article delivery process，Nature Research wishes to improve the reproducibility of the work that we publish, so the researches need to submit a **Reporting Summary** sheet.
2. This sheet includes **Statistical parameters, Software and code, Data, Field-specific reporting, Life sciences study design, Behavioural & social sciences study design, Ecological, evolutionary & environmental sciences study design, Field work, collection and transport, Reporting for specific materials, systems and methods, Unique biological materials, Antibodies, Eukaryotic cell lines, Palaeontology, Animals and other organisms, Human research participants, ChIP-seq, Flow Cytometry, Magnetic resonance imaging.**
3. During the ChIP-seq field, it demands to provide a link to an anonymized genome browser session for "Initial submission" and "Revised version" documnets only, to enable peer revies. Write "no longer applicable" for "Final submission" documents.
4. An `example` of UCSC genome browser session as follows.

## Creating a bigWig track
- Step1: Format the data set. covert your file to bigWig file by utilities. For example wigToBigWig.
- Step2: Move the newly created bigWig file to a `web-accessible http, https, or ftp location`. For example github.
    - 2.1 The file name must ends with a appropriate suffix(.bw).
    - 2.2 Github supports byte-range access to files when they are accessed via the `raw.githubusercontent.com style URLs`.To obtain a raw URL to a file already uploaded on Github, click on a file in your repository and click the Raw button. URL will be shown above.
- Step3: 
  - 3.1 Goto [UCSC](https://genome.ucsc.edu/index.html/), the "Custom Tracks" will be listed in the "My Data". To load a new custom track into the currently displayed track set, click the "add custom tracks" button.
  - 3.2 Construct a custome track using a single track line. The most basic version of the track line will look something like this:
           `track type=bigWig name="My Big Wig" description="A Graph of Data from My Lab" bigDataUrl=http://myorg.edu/mylab/myBigWig.bw`
         - 3.2.1 By fault, the file name will be used to name the track.
         - 3.2.2 You also can click the track "Name" and modify the track, then "submit".
  - 3.3 or paste the URL directly into the text box.
- Step4: Paste this custom track line or URL into the text box in the custom track management page, then click the "submit" button and view the file as a track.
- Step5: (optional) To remove custom tracks from the uploaded track set, click the checkboxes in the "delete" column for all tracks you wish to remove, then click the "delete" button.
- Step6: Click the "My Sessions" listed in the "My Data". During the "Save Settings" field, you should type something into the "name" textbox which will be your session name. Click the checkbox "allow this session to be loaded by others", then "submit".
- Step7: In "My Sessions" field, there will be an entry appear whose name same as Step 6. On the session name, you can right click and copy the URl which is the link you should shared with others.
  - 7.1 The format of URL like this: `http://genome.ucsc.edu/cgi-bin/hgTracks?hgS_doOtherUser=submit&hgS_otherUserName=sessionGallery&hgS_otherUserSessionName=hg19_watsonKriek`
  - 7.2 No login is required to view someelse's saved session, so anyone with this URL can view the session. But no one can change it unless logged in as user.
  - 7.3 The same session name, the same URL.

    :eagle:
