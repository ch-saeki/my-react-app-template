# my-react-app-template
- use typescript.

## nodenv, node, yarn
```
$ brew install nodenv
$ echo 'export PATH="$HOME/.nodenv/bin:$PATH"' >> ~/.bash_profile
$ echo 'eval "$(nodenv init -)"' >> ~/.bash_profile
$ nodenv install {version} # 14.17.5
$ nodenv global {version}  # 14.17.5
$ brew install yarn
```

## create project
```
$ npx create-react-app {project-name} --template typescript
$ cd {project-name}
$ yarn start
```

## set base url
tsconfig.json
```
{
  "compilerOptions": {
    "baseUrl": "src",
    ...,
  }
  ...
}
```

## gh-pages
```
$ yarn add -D gh-pages
```

package.json
```
  // ...
  "homepage": "http://ch-saeki.github.io/my-react-app-template",
  "scripts": {
    // ...
    "deploy": "yarn build && gh-pages -d build"
  },
```
