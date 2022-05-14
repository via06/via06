# This is a basic workflow to help you get started with Actions

name: CI From d38e4c485d19c4392cbdb324885be4c935319be5 Mon Sep 17 00:00:00 2001
From: via06/93613902 <93613902+via06@users.noreply.github.com>
Date: Sat, 14 May 2022 21:06:49 +0800
Subject: [PATCH] Create main.custom.md

---
 main.custom.md | 85 ++++++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 85 insertions(+)
 create mode 100644 main.custom.md

diff --git a/main.custom.md b/main.custom.md
new file mode 100644
index 0000000..63fd9b6
--- /dev/null
+++ b/main.custom.md
@@ -0,0 +1,85 @@
+
+
+On 2022/03/13 12:53:27 Michael Osipov wrote:
+> The Apache Maven team is pleased to announce the release of the Apache
+> Maven 3.8.5
+>
+> Apache Maven is a software project management and comprehension tool.
+> Based on the concept
+> of a project object model (POM), Maven can manage a project's build,
+> reporting and documentation
+> from a central piece of information.
+>
+> Maven 3.8.5 is available via https://maven.apache.org/download.cgi
+>
+> The core release is independent of plugin releases. Further releases of
+> plugins will be made
+> separately.
+>
+> If you have any questions, please consult:
+>
+> - the web site: https://maven.apache.org/
+> - the maven-user mailing list: https://maven.apache.org/mailing-lists.html
+> - the reference documentation: https://maven.apache.org/ref/3.8.5/
+>
+>
+> Release Notes - Maven - Version 3.8.5
+>
+> ** Bug
+>      * [MNG-5180] - Versioning's snapshot version list is not included
+> in metadata merge
+>      * [MNG-5561] - Plugin relocation loses configuration
+>      * [MNG-5982] - The POM for ... is invalid, transitive dependencies
+> ... while property was overriden
+>      * [MNG-6326] - Build continues when core extensions aren't found
+>      * [MNG-6727] - Using version range in parent and CI Friendly
+> Version fails
+>      * [MNG-6802] - FileProfileActivator changes
+> FileProfileActivator.exists which lets flattened resolveCiFriendliesOnly
+> depending fail activating profile
+>      * [MNG-7156] - Parallel build can cause issues between clean and
+> forked goals
+>      * [MNG-7335] - [Regression] Parallel build fails due to missing JAR
+> artifacts in compilePath
+>      * [MNG-7347] - SessionScoped beans should be singletons for a given
+> session
+>      * [MNG-7357] - All Maven Core JARs have unusual entry order
+>      * [MNG-7362] - DefaultArtifactResolver has spurious "Failure
+> detected" INFO log
+>      * [MNG-7374] - Mutating RelocatedArtifact does not retain type
+>      * [MNG-7386] - ModelMerger$MergingList is not serializable
+>      * [MNG-7402] - BuildListCalculator never detaches the classloader
+>      * [MNG-7417] - Several classes do not set properties properly for
+> building requests
+>
+> ** New Feature
+>      * [MNG-7395] - Support interpolation in extensions.xml
+>      * [MNG-7407] - Introduce a ModelVersionProcessor component to make
+> CI Friendly Versions pluggable
+>
+> ** Improvement
+>      * [MNG-6960] - Use RuntimeInformation instead of reading properties
+>      * [MNG-7349] - Limit relocation warning message to direct
+> dependencies only
+>      * [MNG-7380] - Don't log non-threadsafe warning if only building a
+> single module
+>      * [MNG-7381] - Shorten parallel builder thread name to artifactId,
+> conditionally with groupId
+>      * [MNG-7385] - Improve documentation on repository metadata
+>      * [MNG-7400] - Allow more WorkspaceReaders to participate
+>      * [MNG-7408] - Explain reporting plugin version automatic selection
+> (in Maven 3)
+>
+> ** Dependency upgrade
+>      * [MNG-7370] - Upgrade Maven Wagon to 3.5.1
+>      * [MNG-7384] - Upgrade Maven JAR Plugin to 3.2.2
+>      * [MNG-7428] - Upgrade Maven Parent to 35
+>
+>
+> For more information read
+> https://maven.apache.org/docs/3.8.5/release-notes.html
+>
+> Enjoy!
+>
+> - The Maven Team
+>  

# Controls when the workflow will run
on:
  # Triggers the workflow on push or pull request events but only for the master branch
  push:
    branches: [ main.custom.md ]
  pull_request:
    branches:[ main.custom.md]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# A workflow run is made up of one or more jobs that can run sequentially or in parallel
jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest

    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: actions/checkout@v3

      # Runs a single command using the runners shell
      - name: Run a one-line script
        run: echo Hello, world!

      # Runs a set of commands using the runners shell
      - name: Run a multi-line script
        run: |
          echo Add other actions to build,
          echo test, and deploy your project.
