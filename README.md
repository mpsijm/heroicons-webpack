# heroicons-webpack

This repository demonstrates tree-shaking for the `@heroicons/react` module. In this example [webpack](https://webpack.js.org/) is used to bundle the `src/index.js` file and output it to `dist/main.js`. The source file imports a single icon from `@heroicons/react`.

### Build instructions

```
npm install
npm run build
```

After building you can see that only one icon is included in the output bundle. The entire bundle is included below (formatted):

<details>
  <summary>Bundle code</summary>

```js
;(() => {
  'use strict'
  var e,
    t = {
      418: (e) => {
        var t = Object.getOwnPropertySymbols,
          r = Object.prototype.hasOwnProperty,
          o = Object.prototype.propertyIsEnumerable
        function n(e) {
          if (null == e)
            throw new TypeError('Object.assign cannot be called with null or undefined')
          return Object(e)
        }
        e.exports = (function () {
          try {
            if (!Object.assign) return !1
            var e = new String('abc')
            if (((e[5] = 'de'), '5' === Object.getOwnPropertyNames(e)[0])) return !1
            for (var t = {}, r = 0; r < 10; r++) t['_' + String.fromCharCode(r)] = r
            if (
              '0123456789' !==
              Object.getOwnPropertyNames(t)
                .map(function (e) {
                  return t[e]
                })
                .join('')
            )
              return !1
            var o = {}
            return (
              'abcdefghijklmnopqrst'.split('').forEach(function (e) {
                o[e] = e
              }),
              'abcdefghijklmnopqrst' === Object.keys(Object.assign({}, o)).join('')
            )
          } catch (e) {
            return !1
          }
        })()
          ? Object.assign
          : function (e, a) {
              for (var i, c, f = n(e), s = 1; s < arguments.length; s++) {
                for (var p in (i = Object(arguments[s]))) r.call(i, p) && (f[p] = i[p])
                if (t) {
                  c = t(i)
                  for (var u = 0; u < c.length; u++) o.call(i, c[u]) && (f[c[u]] = i[c[u]])
                }
              }
              return f
            }
      },
      408: (e, t, r) => {
        var o = r(418),
          n = 60103
        if ('function' == typeof Symbol && Symbol.for) {
          var a = Symbol.for
          ;(n = a('react.element')),
            a('react.portal'),
            a('react.fragment'),
            a('react.strict_mode'),
            a('react.profiler'),
            a('react.provider'),
            a('react.context'),
            a('react.forward_ref'),
            a('react.suspense'),
            a('react.memo'),
            a('react.lazy')
        }
        'function' == typeof Symbol && Symbol.iterator
        function i(e) {
          for (
            var t = 'https://reactjs.org/docs/error-decoder.html?invariant=' + e, r = 1;
            r < arguments.length;
            r++
          )
            t += '&args[]=' + encodeURIComponent(arguments[r])
          return (
            'Minified React error #' +
            e +
            '; visit ' +
            t +
            ' for the full message or use the non-minified dev environment for full errors and additional helpful warnings.'
          )
        }
        var c = {
            isMounted: function () {
              return !1
            },
            enqueueForceUpdate: function () {},
            enqueueReplaceState: function () {},
            enqueueSetState: function () {},
          },
          f = {}
        function s(e, t, r) {
          ;(this.props = e), (this.context = t), (this.refs = f), (this.updater = r || c)
        }
        function p() {}
        function u(e, t, r) {
          ;(this.props = e), (this.context = t), (this.refs = f), (this.updater = r || c)
        }
        ;(s.prototype.isReactComponent = {}),
          (s.prototype.setState = function (e, t) {
            if ('object' != typeof e && 'function' != typeof e && null != e) throw Error(i(85))
            this.updater.enqueueSetState(this, e, t, 'setState')
          }),
          (s.prototype.forceUpdate = function (e) {
            this.updater.enqueueForceUpdate(this, e, 'forceUpdate')
          }),
          (p.prototype = s.prototype)
        var l = (u.prototype = new p())
        ;(l.constructor = u), o(l, s.prototype), (l.isPureReactComponent = !0)
        var d = null,
          h = Object.prototype.hasOwnProperty,
          y = { key: !0, ref: !0, __self: !0, __source: !0 }
        t.createElement = function (e, t, r) {
          var o,
            a = {},
            i = null,
            c = null
          if (null != t)
            for (o in (void 0 !== t.ref && (c = t.ref), void 0 !== t.key && (i = '' + t.key), t))
              h.call(t, o) && !y.hasOwnProperty(o) && (a[o] = t[o])
          var f = arguments.length - 2
          if (1 === f) a.children = r
          else if (1 < f) {
            for (var s = Array(f), p = 0; p < f; p++) s[p] = arguments[p + 2]
            a.children = s
          }
          if (e && e.defaultProps) for (o in (f = e.defaultProps)) void 0 === a[o] && (a[o] = f[o])
          return { $$typeof: n, type: e, key: i, ref: c, props: a, _owner: d }
        }
      },
      294: (e, t, r) => {
        e.exports = r(408)
      },
    },
    r = {}
  function o(e) {
    var n = r[e]
    if (void 0 !== n) return n.exports
    var a = (r[e] = { exports: {} })
    return t[e](a, a.exports, o), a.exports
  }
  ;(e = o(294)),
    console.log(function (t) {
      return e.createElement(
        'svg',
        Object.assign(
          {
            xmlns: 'http://www.w3.org/2000/svg',
            viewBox: '0 0 20 20',
            fill: 'currentColor',
            'aria-hidden': 'true',
          },
          t
        ),
        e.createElement('path', {
          fillRule: 'evenodd',
          d: 'M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z',
          clipRule: 'evenodd',
        })
      )
    })
})()
```

</details>
