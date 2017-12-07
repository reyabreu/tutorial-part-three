# gatsby-tutorial-part-three
Skeleton content with the bare essentials needed for a [Gatsby](https://www.gatsbyjs.org/) tutorial site

Install this project (assuming Gatsby is installed) by running from your CLI:
```
gatsby new tutorial-part-three https://github.com/gatsbyjs/gatsby-starter-hello-world
```

Needs typography.js plugin installation as well using the Fairy Gates theme:
```
npm install --save gatsby-plugin-typography typography-theme-fairy-gates
```
after this is completed, you will need a custom `gatsby-config.js` file as to activate the plugin
```
module.exports = {
  plugins: [
    {
      resolve: `gatsby-plugin-typography`,
      options: {
        pathToConfigModule: `src/utils/typography.js`,
      },
    },
  ],
};
```
don't forget to fill in a `src\utils\typography.js` file with your custom options.
```
import Typography from "typography";
import fairyGateTheme from "typography-theme-fairy-gates";

const typography = new Typography(fairyGateTheme);

export default typography;
```
## Running in development
`gatsby develop`

## deployment
(first time only)
```
echo reyabreu.surge.sh > public\CNAME
```
to upload
```
surge public
```