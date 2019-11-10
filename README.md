# ProgressBarRTLInXamarin
This is a repo to test the RTL capabilities of the ProgressBar view in Xamarin.Forms.
The `ProgressBar.FlowDirection` property of the ProgreesBar in MainPage is set to `RightToLeft`. So, it should progress from right to left.
At first, it didn't work. The problem was that - for Android - we need to put `android:supportsRtl` attribute in the AndroidManifest.xml file; only I put it in the wrong place, as an attribute of the `manifest` element, while it is an attribute of the `application` element.
After the change, the ProgressBar properly progress from right to left when its `FlowDirection`is set to `RightToLeft`.
