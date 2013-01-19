Update in Git

Add device id
  developer.apple.com
  download the provisioning profile
  double click to add to xcode
  remove old ad-hoc profile
  upload the new profile to testflight *not sure if this is necessary 1/18

Change CFBundleVersion or CFBundleShortVersionString.
TestFlight https://testflightapp.com/dashboard/
  Change the build target from iPad/iPhone Simulator to iOS Device
  In build settings, change to use the new provisioning profile
  Under the Product menu, select Archive. This will build your application and code sign it using the Distribution (Ad Hoc or App Store) profile setup in step 5 of the “Creating the Basic Application” section. Once the build has completed the Organizer window will appear. If it does not, open it using CMD-Shift–2 or Window -> Organizer. If you see a message popup saying “codesign wants to sign using key ”privateKey“ in your keychain.”, select Allow or Always Allow.
  Go to the Archives tab in Organizer and select your application, if it was not automatically selected, and choose the archive you wish to share.
  Click the Distribute button. In the next window select “Save for Enterprise or Ad-Hoc Deployment”, and click Next.
  In the Code Signing Identity drop down, select the same Distribution Provisioning Profile specified in the Release configuration from step 5 of the “Creating the Basic Application” section, and click Next. NOTE: When generating an IPA for distribution on TestFlight, you should always use an Ad Hoc Distribution Provisioning Profile for both the Archive and Distribute options.
  Select where you would like to save your IPA and upload to TestFlight.
