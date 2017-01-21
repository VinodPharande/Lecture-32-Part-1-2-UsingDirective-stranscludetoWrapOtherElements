# Lecture-32-Part-1-2-UsingDirective-stranscludetoWrapOtherElements
Lecture-32-Part-1-2-UsingDirective’stranscludetoWrapOtherElements


----------------------------------------------------------------------------------------------------------------------
Lecture 32, Part 1: Using Directive’s transclude to Wrap Other Elements
- Step-1: Set transclude to true
	function MyDirective(){
		var ddo = {
			scope: {
			},
			transclude: true,
			templateUrl: 'template.html'
		};
		return ddo;
	}
- Step-2: Wrap some parent content
	<my-directive>
		<span>
			WARNING! WARNING! {{ctrl.someProp}}
		</span>
	</my-directive>
	// ctrl.someProp: Evaluated in the parent controller, not in our directive
- Step-3: ng-transclude To place wrapped content
	<div>
		<div ng-transclude></div>
	</div>
	// ng-transclude: Insert evaluated wrapped content into element marked with ng-transclude

----------------------------------------------------------------------------------------------------------------------
Lecture 32, Part 2: Using Directive’s transclude to Wrap Other Elements
- transclude allows whole templates to be passed into a directive.
- The wrapped content is evaluated in the parent's context, NOT in the directive's context.
- In the DDO:
	- transclude: true
- In directive's template:
	- ng-transclude attribute designates place for evaluated wrapped content.
----------------------------------------------------------------------------------------------------------------------
