# Angular Project Setup

## References

[Angular CLI - Github readme.md](https://github.com/angular/angular-cli)

## **Update Node and Angualar CLI -** _**Optional**_

### **Update Node**

1. Check current version at command line: `>node --version`
2. Download newer node installer at [nodejs.org](https://nodejs.org/en/)
3. Run installer
4. Update npm \(optional\): `npm install -g npm`

### Update Angular CLI

In terminal check the currently installed Angular version:  

```text
ng --version
```

In terminal check the latest npm version number:

```text
npm show @angular/cli version
```

If newer version is required, run the following npm commands:  

```text
npm uninstall -g @angular/cli
npm cache verify
# if npm version is < 5 then use `npm cache clean`
npm install -g @angular/cli@latest
```

Can check the version with:

```text
npm -g list --depth=0
```

## **Create New App**

Navigate to directory where new project should be created \(as a new subdirectory\), then:

```text
ng new my-app
```

