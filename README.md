## Talk Title: Signals- The Gem of May :gem: :gem: :gem:
_Why choose this name although now is September? Because Signals is the new feature of Angular 16, which is released on May 2023._
### Talk Description: ~ 15 mins
#### 1.	**5W1H** in Signals.
:point_right: _We will talk about: Why, What, How, Where, When._
  - Why do we need Signals?
  - What is a Signals?
  - How to create a Signals?
  - When to use Signals?
  - Where can we use signals?
#### 2.	Why not continue with zone.js?
:point_right: _Mainly talk about signals and zone.js._
- We will clarify the question: “Will Signals lead to zone.js being optional?”.
- Drawbacks of zone.js: Angular depends on zone.js to trigger change detection. zoneJs will send a signal and notify Angular. As a result, Angular does not know where those events occur. Therefore, it need to run change detection from top to bottom in the component tree.
#### 3.	Are we going to have another change detection strategy?
:point_right: _Talk about change detection._
- Because Angular runs change detection from the top to bottom. That is the reason why we have OnPush. 
- But OnPush Strategy also has its own drawbacks, too.
  - As we’ve known, OnPush change detection provides the possibility to skip unnecessary checks for the component and all its children components.
  - But when we use **detectChange()** or **markForCheck()**, it breaks the rules. 
    - detectChanges runs change detection immediately from the current component down through its children.
    - markForCheck marks current component and its parents up to the root as dirty for the next tick. 
  - But it should be **only components** that read an updated signal that will have to be change-detected.
    - None of its parents and none of its children.
    - One and only one component that needs to display changed data
- So, the question is: “Are we going to have another change detection strategy?”.
- :heavy_check_mark:	 That’s a problem that Signals solves for us.
#### 4.	Manage RxJS traffic with Signals.
:point_right: _Talk about signals and RxJS._
- Problems: 2 subscribers to 1 Observable.
  - :sneezing_face: Old solution: using shareReplay()
  - :smile: New solution: Signals
- Reason: Maybe team does not adapt with RxJS, etc,...
#### 5. Demo :computer: ~10 - 15mins
#### Other informations:
- Expected present time: 30mins
- Speaker Bio: [https://www.linkedin.com/in/tranntn/]
- Profile Photo URL: Update later...
