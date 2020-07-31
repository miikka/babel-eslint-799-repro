This repo aims to reproduce the issue [babel/babel-eslint#799](https://github.com/babel/babel-eslint/issues/799).

To try it yourself:

```sh
git clone https://github.com/miikka/babel-eslint-799-repro
cd babel-eslint-799-repro
npm ci
npm test
```

Here's what I get when I run it myself:

```
% npm test

> babel-eslint-799-repro@1.0.0 test /Users/miikka/mess/2020-31/babel-eslint-799-repro
> eslint index.js


Oops! Something went wrong! :(

ESLint: 7.5.0

TypeError: Cannot read property 'value' of null
Occurred while linting /Users/miikka/mess/2020-31/babel-eslint-799-repro/index.js:1
    at checkSpacingBefore (/Users/miikka/mess/2020-31/babel-eslint-799-repro/node_modules/eslint/lib/rules/template-curly-spacing.js:52:24)
    at TemplateElement (/Users/miikka/mess/2020-31/babel-eslint-799-repro/node_modules/eslint/lib/rules/template-curly-spacing.js:136:17)
    at /Users/miikka/mess/2020-31/babel-eslint-799-repro/node_modules/eslint/lib/linter/safe-emitter.js:45:58
    at Array.forEach (<anonymous>)
    at Object.emit (/Users/miikka/mess/2020-31/babel-eslint-799-repro/node_modules/eslint/lib/linter/safe-emitter.js:45:38)
    at NodeEventGenerator.applySelector (/Users/miikka/mess/2020-31/babel-eslint-799-repro/node_modules/eslint/lib/linter/node-event-generator.js:254:26)
    at NodeEventGenerator.applySelectors (/Users/miikka/mess/2020-31/babel-eslint-799-repro/node_modules/eslint/lib/linter/node-event-generator.js:283:22)
    at NodeEventGenerator.enterNode (/Users/miikka/mess/2020-31/babel-eslint-799-repro/node_modules/eslint/lib/linter/node-event-generator.js:297:14)
    at CodePathAnalyzer.enterNode (/Users/miikka/mess/2020-31/babel-eslint-799-repro/node_modules/eslint/lib/linter/code-path-analysis/code-path-analyzer.js:673:23)
    at /Users/miikka/mess/2020-31/babel-eslint-799-repro/node_modules/eslint/lib/linter/linter.js:949:32
npm ERR! Test failed.  See above for more details.
```
