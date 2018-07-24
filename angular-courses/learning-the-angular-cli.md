# Learning the Angular CLI

## Learning the Angular CLI

### Info

* **Source**: LinkedInLearning
* **Course**: [Learning the Angular CLI](https://www.linkedin.com/learning/learning-the-angular-cli-2)
* **Author**: Victor Mejia

### Commands

#### Help

```text
>ng help
>ng --version
>ng <command> --help --> example  >ng generate class --help
```

#### New

```text
>ng new --help
>ng new contact-manager --routing --prefix=mk --style=scss --skip-install --dry-run
```

> Environments directory can be used for environment specific data: `>ng build --environment=<env>` : the options are defined in .angular-cli.json file import environment in js module : `import { environment } from './environments/environment';`

#### Serve

```text
>ng serve --help
>ng serve --open
>ng serve --open --port=8000
```

> **Custom Domain**
>
> 1. edit hosts file \(windows: C:\Windows\System32\drivers\etc\hosts\) ex: add line - 127.0.0.1 localhost.dev.company.com
> 2. `ng serve --open --host=localhost.dev.company.com --port=8001` can create an npm script --&gt; "start": "ng serve --open --host=localhost.dev.company.com --port=8001"

> **proxy with webpack-dev-server**
>
> 1. See course exercise files ch03 --&gt; 03-03 --&gt; end
> 2. Uses proxy.conf.json to config proxy
> 3. Modified npm script: "start": "ng serve --proxy-config proxy.conf.json --open"

#### Generate

```text
>ng generate [schematic] [name] <options...>
>ng generate --help
>ng generate component contact-list --dry-run -- or -- ng g c contact-list --dry-run

>ng generate module shared --module app --dry-run
>ng generate directive shared/directives/non-numeric --module=shared
>ng g m services --module=app
>ng generate service services/api --module=services
>ng g m pipes --module=app
>ng generate pipe pipes/phone --module=pipes --export
>ng generate class models/contact 
>ng generate interface models/icontact
>ng generate enum models/contact-type
>ng generate guard auth
```

#### Build

```text
>ng build --help
>ng build
>ng build --prod --sourcemap
```

> `ng build --prod --stats-json`  
> generates a stats.json file that can be used to analyse bundle \([https://webpack.github.io/analyse/](https://webpack.github.io/analyse/)\)

#### Testing

Change browser in karma.conf.js file via "Browsers" array  
For example: \`browsers: \['ChromeHeadless'\]

> For ChromeHeadless, need to install a reporter:
>
> 1. `npm install karma-spec-reporter --savedev`
> 2. add require\('karma-spec-reporter'\) to the karma.conf.js "plugins" array
> 3. add new item 'text-summary' to the coverageInstanbulReporter reports: array
> 4. modify reporters: array to \['spec', 'kjhtml'\] \(replace 'progress' with 'spec'\)
> 5. modify npm script: "test": "ng test --single-run --code-coverage"

### Other Info

#### Assets Config

Can add additional assets to copy to the dist folder, for example:

```text
  "assets": {
    "glob": **/*,
    "input": "../node_modules/weather-underground-icons/dist/icons/black/png/32x32",
    "output": "./weather-icons"
  }
```

> With this in the .angular-cli.json file, the icons will be copied to the ./dist/weather-icons directory

#### CSS Framework Config

Can add an additional framework via the .angular-cli.json file "styles" array:

```text
"styles": [
  "styles.scss",
  "./node_modules/bootstrap/dist/css/bootstrap.min.css"
]
```

> With this in place the bootstrap file will be added as a global style to app - with this in place the bootstrap file will be added as a global style to app

#### Javascript Library Config

Can add javascript files to the global scope via the .angular-cli.json file "scripts" arra:

```text
"scripts": [
  "./node_modules/particles.js/particles.js"
]
```

#### Route Guards

See exercise files ch04 --&gt; 04-08 --&gt; begin  
`>ng generate guard auth`

