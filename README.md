# react-sass

## 安装依赖

```bash
npm install sass-loader node-sass --save-dev
```

## 改动部分

### webpack.config.dev.js

```js
// 139
  // Add .scss to exclude array
  /\.scss$/,
// 142
...
// 213
{
  test: /\.scss$/,
  include: paths.appSrc,
  loaders: [require.resolve('style-loader'), require.resolve('css-loader'), require.resolve('sass-loader')]
}
// 219
```

### Rename `App.css` to `App.scss`

### App.js

```js
import './App.scss';

class App extends Component {
  render() {
    return (
      <div className="App">
        <div className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <h2>Welcome to React</h2>
        </div>
        <p className="App-intro">
          To get started, edit <code>src/App.js</code> and save to reload.
        </p>
      </div>
    );
  }
}
```
