All gizmos here are allowed to carry dependencies from /gear

Only outputted dependencies allowed in /gizmo-public

Classes are defined according the following example.
This is done to avoid abusive usage of classes;
Only 1 level deep [object level], avoid deeper levels like:

[!not cool -> bl-form-label-mark]

.bl-form {

	label,
	.bl-form-label {

		.bl-form-mark {

		}
	}
}
.bl-form label,
.bl-form .bl-form-label
.bl-form .bl-form-label .bl-form-mark {
	
}

bl-form-label [belongs to] bl-form
bl-form-mark [belongs to] bl-form-label


tl-variations is a combination of multiple single objects that are able to be combined in a way

levels 1 2 3 are dependency levels;

3 are dependent of level 2,
3 and 2 are dependent of level 1

order of types of css
1. scope variables, mixins and functions within a file are declared first
2. second are structure css, note these css contains only the structure css and therefor allowed to be nested 
3. all objects css are declared under 1 and 2, maintain minimal dependencies.


modifiers such as tl-large can never act autonomously and should combined with object classes to define / declare itself

.tl-fixed, .tl-small, .tl-medium, .tl-large are modifiers not allowed to put ass single class

vendor specifics added;