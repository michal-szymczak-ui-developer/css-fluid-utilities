
## Fluid CSS Utility classes in your work
Add to you project a list of CSS classes for fluid font sizes and spacers (paddings, margins, gaps) similiar to utopia.fyi.

###Usage
-----------------------------------
`$ npm install --save-dev css-fluid-utilities`

Import files and add your customizastion (optionally) in right order:
```
@import "./node_modules/css-fluid-utilities/scss/functions";

/* Add customizations - Optionally (described below) */

@import "./node_modules/css-fluid-utilities/scss/settings";
@import "./node_modules/css-fluid-utilities/scss/utilities";
```
###Customization
-----------------------------------
1. **Change breakpoints** (must be SCSS variables)
``` 
$fluid-min-resolution: 420px;
$fluid-max-resolution: 1440px;	
```

2. Define **SPACERS** CSS variables and map (map is used to generate classes)
```
:root {
  	--fluid-spacer-100: #{g-fluid(4px, 8px)};
  	--fluid-spacer-200: #{g-fluid(6px, 12px)};
  	--fluid-spacer-300: #{g-fluid(8px, 16px)};
  	--fluid-spacer-400: #{g-fluid(12px, 24px)};
  	--fluid-spacer-500: #{g-fluid(16px, 32px)};
  	--fluid-spacer-600: #{g-fluid(24px, 48px)};
  	--fluid-spacer-700: #{g-fluid(32px, 64px)};
  	--fluid-spacer-800: #{g-fluid(48px, 96px)};
  	--fluid-spacer-900: #{g-fluid(96px, 128px)};
  	--fluid-spacer-1000: #{g-fluid(128px, 256px)};
}
 
 $fluid-spacers: (
	100: var(--fluid-spacer-100),
	200: var(--fluid-spacer-200),
	300: var(--fluid-spacer-300),
	400: var(--fluid-spacer-400),
	500: var(--fluid-spacer-500),
	600: var(--fluid-spacer-600),
	700: var(--fluid-spacer-700),
	800: var(--fluid-spacer-800),
	900: var(--fluid-spacer-900),
	1000: var(--fluid-spacer-1000),
);
```
3. Define **FONT SIZES** CSS variables and map (map is used to generate classes)
```
:root {
	--fluid-fs-100: #{g-fluid(8px, 10px)};
	--fluid-fs-200: #{g-fluid(10px, 12px)};
	--fluid-fs-300: #{g-fluid(12px, 14px)};
	--fluid-fs-400: #{g-fluid(14px, 16px)};
	--fluid-fs-500: #{g-fluid(16px, 18px)};
	--fluid-fs-600: #{g-fluid(16px, 22px)};
	--fluid-fs-700: #{g-fluid(18px, 24px)};
	--fluid-fs-800: #{g-fluid(20px, 28px)};
	--fluid-fs-900: #{g-fluid(24px, 38px)};
	--fluid-fs-1000: #{g-fluid(32px, 58px)};
}
 
 $fluid-font-sizes: (
	100: var(--fluid-fs-100),
	200: var(--fluid-fs-200),
	300: var(--fluid-fs-300),
	400: var(--fluid-fs-400),
	500: var(--fluid-fs-500),
	600: var(--fluid-fs-600),
	700: var(--fluid-fs-700),
	800: var(--fluid-fs-800),
	900: var(--fluid-fs-900),
	1000: var(--fluid-fs-1000),
);
```
