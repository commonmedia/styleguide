# Developing SCSS applications

## Coding Style
* Project Structure
1. Be as specific as possible.
2. Use as many seperate files as necessary
3. Seperate components and abstract styles as much as possible
4. Indent properly and consistantly
5. Try to have css properties be in as close to alphabetical order as is reasonable
6. One line per property

Styleguide Example Code

```
	.myClass {
		/* put properties that apply directly to class at the top.  Mixins first followed by normal CSS */
		@include border-radius(4px);
		@include box-shadow(0 20px 0 #000);
		@include inline-block;
		color:red;
		float:left;
		width:100%;

		/* psuedo selectors that apply directly to the class are next */
		&:hover, &:focus {
			color:green;
		}

		/* followed by child classes/descendants */
		> span.mySubClass {
			@include inline-block;
			position:absolute;
			top:0px;
			
			&.right {
				right:0;
			}

			&.left {
				left:0;
			}
		}

		.myClass-header {
			font-size:20px;
			font-weight:600;
			line-height:24px;
		}

	}

```
