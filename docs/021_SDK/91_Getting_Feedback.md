User feedback can be vital and contain highly relevant information when it comes to improving your app experience. Make it easier for your testers to communicate with you and send you their thoughts on how to make your app better.

TestFairy provides an easy way to collect this feedback. If you've [added the TestFairy SDK](https://docs.testfairy.com/SDK/Adding_The_SDK_To_Your_App.html) to your app, then all you need to do is enable the **In-App Bug Reporting** feature in your build settings.

![alt](../../img/sdk/enable_feedback.png)

When you beta testers shake their device, they will be prompted to report a feedback, which will be added to the existing session. All feedback include videos, device informations, app logs and an event timeline so you can easily reproduce each problem.

If you'd rather have control over how your testers provide feedback (maybe your app is already using shake for other purposes), you can programmaitcally display the feedback form in a way that best suits your app's experience. A typical use case may be to call the method when your tester taps a button in your app settings, or after a tester passes a given page in your app.

Note that if you choose to programmaitcally display the feedback form, you _do not_ need to have **In-App Bug Reporting** enabled.

<div data-duration-in="300" data-duration-out="100" class="docs-tabs w-tabs">
	<div class="docs-tabs-menu w-tab-menu" style="flex-wrap: wrap;">
		<a data-w-tab="tab-android" class="docs-tab w-inline-block w-tab-link w--current" style="margin: 2px;" href="#android">
			<div>Android</div>
		</a>
		<a data-w-tab="tab-ios" class="docs-tab w-inline-block w-tab-link" style="margin: 2px;" href="#ios">
			<div>iOS</div>
		</a>
		<a data-w-tab="tab-cordova" class="docs-tab w-inline-block w-tab-link" style="margin: 2px;" href="#cordova">
			<div>Cordova</div>
		</a>
		<a data-w-tab="tab-react-native" class="docs-tab w-inline-block w-tab-link" style="margin: 2px;" href="#react-native">
			<div>React Native</div>
		</a>
		<a data-w-tab="tab-nativescript" class="docs-tab w-inline-block w-tab-link" style="margin: 2px;" href="#nativescript">
			<div>Nativescript</div>
		</a>
		<a data-w-tab="tab-xamarin" class="docs-tab w-inline-block w-tab-link" style="margin: 2px;" href="#xamarin">
			<div>Xamarin</div>
		</a>
		<a data-w-tab="tab-unity" class="docs-tab w-inline-block w-tab-link" style="margin: 2px;" href="#unity">
			<div>Unity</div>
		</a>
		<a data-w-tab="tab-adobe-air" class="docs-tab w-inline-block w-tab-link" style="margin: 2px;" href="#adobe-air">
			<div>Adobe Air</div>
		</a>
	</div>

	<div class="docs-tabs-content w-tab-content">
		<div data-w-tab="tab-android" class="w-tab-pane w--tab-active">
			<h3>Syntax</h3>
      <p>
				<b>TestFairy.showFeedbackForm();</b><br />
      </p>

      <h3>Code Example</h3>
      <pre>
// Be sure to import TestFairy
import com.testfairy.TestFairy;

// Can be invoked on a button press
// or after your app passes a given page
TestFairy.showFeedbackForm();
      </pre>
		</div>

		<div data-w-tab="tab-ios" class="w-tab-pane">
			<h3>Syntax</h3>
			<p>
				<b>[TestFairy pushFeedbackController];</b><br />
			</p>

			<h3>Code Example</h3>
			<pre>
// Be sure to import TestFairy
#import "TestFairy.h"

// Can be invoked on a button press
// or after your app passes a given page
[TestFairy pushFeedbackController];
			</pre>

			<h4>Note</h4>
			<p>On iOS, if the <b>In-App Bug Reporting</b> feature is enabled, the feedback form will also be shown when the tester takes a screenshot.</p>
		</div>

		<div data-w-tab="tab-cordova" class="w-tab-pane">
			<h3>Syntax</h3>
      <p>
				<b>TestFairy.pushFeedbackController();</b><br />
      </p>

      <h3>Code Example</h3>
      <pre>
// Can be invoked on a button press
// or after your app passes a given page
TestFairy.pushFeedbackController();
      </pre>
		</div>

		<div data-w-tab="tab-react-native" class="w-tab-pane">
			<h3>Syntax</h3>
      <p>
				<b>TestFairy.pushFeedbackController();</b><br />
      </p>

      <h3>Code Example</h3>
      <pre>
// Be sure to import TestFairy
const TestFairy = require('react-native-testfairy');

// Can be invoked on a button press
// or after your app passes a given page
TestFairy.pushFeedbackController();
      </pre>
		</div>


		<div data-w-tab="tab-nativescript" class="w-tab-pane">
			<h3>Syntax</h3>
      <p>
				<b>TestFairySDK.pushFeedbackController();</b><br />
      </p>

      <h3>Code Example</h3>
      <pre>
// Be sure to import TestFairy
import { TestFairySDK } from 'nativescript-testfairy';

// Can be invoked on a button press
// or after your app passes a given page
TestFairySDK.pushFeedbackController();
      </pre>
		</div>

		<div data-w-tab="tab-xamarin" class="w-tab-pane">
			<h3>Syntax</h3>
      <p>
				<b>TestFairy.SetUserId ("&lt;userId&gt;");</b><br />
      </p>

      <h3>Code Example</h3>
      <pre>
// Be sure to import TestFairy
using TestFairyLib;

// Can be invoked on a button press
// or after your app passes a given page
TestFairy.PushFeedbackController();
      </pre>
		</div>

		<div data-w-tab="tab-unity" class="w-tab-pane">
			<h3>Syntax</h3>
      <p>
				<b>TestFairy.pushFeedbackController();</b><br />
      </p>

      <h3>Code Example</h3>
      <pre>
// Be sure to import TestFairy
using TestFairyUnity;

// Can be invoked on a button press
// or after your app passes a given page
TestFairy.pushFeedbackController();
      </pre>
		</div>

		<div data-w-tab="tab-adobe-air" class="w-tab-pane">
			<h3>Syntax</h3>
      <p>
				<b>AirTestFairy.pushFeedbackController();</b><br />
      </p>

      <h3>Code Example</h3>
      <pre>
// Be sure to import TestFairy
import com.testfairy.AirTestFairy;

// Can be invoked on a button press
// or after your app passes a given page
AirTestFairy.pushFeedbackController();
      </pre>
		</div>

	</div>
</div>
