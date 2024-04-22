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
(() => {
  "use strict";
  var e = {
    228: e => {
      var t = Object.getOwnPropertySymbols,
          r = Object.prototype.hasOwnProperty,
          o = Object.prototype.propertyIsEnumerable;
      e.exports = function() {
        try {
          if (!Object.assign) return !1;
          var e = new String("abc");
          if (e[5] = "de", "5" === Object.getOwnPropertyNames(e)[0])
            return !1;
          for (var t = {}, r = 0; r < 10; r++) t["_" + String
                                                 .fromCharCode(r)] = r;
          if ("0123456789" !== Object.getOwnPropertyNames(t).map((
            function(e) {
              return t[e]
            })).join("")) return !1;
          var o = {};
          return "abcdefghijklmnopqrst".split("").forEach((function(e) {
            o[e] = e
          })), "abcdefghijklmnopqrst" === Object.keys(Object
                                                      .assign({}, o)).join("")
        } catch (e) {
          return !1
        }
      }() ? Object.assign : function(e, n) {
        for (var a, i, c = function(e) {
          if (null == e) throw new TypeError(
            "Object.assign cannot be called with null or undefined"
          );
          return Object(e)
        }(e), f = 1; f < arguments.length; f++) {
          for (var l in a = Object(arguments[f])) r.call(a, l) && (c[
            l] = a[l]);
          if (t) {
            i = t(a);
            for (var s = 0; s < i.length; s++) o.call(a, i[s]) && (c[i[
              s]] = a[i[s]])
          }
        }
        return c
      }
    },
    287: (e, t, r) => {
      var o = r(228),
          n = 60103,
          a = 60112;
      if ("function" == typeof Symbol && Symbol.for) {
        var i = Symbol.for;
        n = i("react.element"), i("react.portal"), i("react.fragment"), i(
          "react.strict_mode"), i("react.profiler"), i(
          "react.provider"), i("react.context"), a = i(
          "react.forward_ref"), i("react.suspense"), i("react.memo"), i(
          "react.lazy")
      }
      "function" == typeof Symbol && Symbol.iterator;

      function c(e) {
        for (var t =
             "https://reactjs.org/docs/error-decoder.html?invariant=" + e,
             r = 1; r < arguments.length; r++) t += "&args[]=" +
          encodeURIComponent(arguments[r]);
        return "Minified React error #" + e + "; visit " + t +
          " for the full message or use the non-minified dev environment for full errors and additional helpful warnings."
      }
      var f = {
        isMounted: function() {
          return !1
        },
        enqueueForceUpdate: function() {},
        enqueueReplaceState: function() {},
        enqueueSetState: function() {}
      },
          l = {};

      function s(e, t, r) {
        this.props = e, this.context = t, this.refs = l, this.updater =
          r || f
      }

      function u() {}

      function p(e, t, r) {
        this.props = e, this.context = t, this.refs = l, this.updater =
          r || f
      }
      s.prototype.isReactComponent = {}, s.prototype.setState = function(
        e, t) {
        if ("object" != typeof e && "function" != typeof e && null != e)
          throw Error(c(85));
        this.updater.enqueueSetState(this, e, t, "setState")
      }, s.prototype.forceUpdate = function(e) {
        this.updater.enqueueForceUpdate(this, e, "forceUpdate")
      }, u.prototype = s.prototype;
      var d = p.prototype = new u;
      d.constructor = p, o(d, s.prototype), d.isPureReactComponent = !0;
      var h = null,
          y = Object.prototype.hasOwnProperty,
          v = {
            key: !0,
            ref: !0,
            __self: !0,
            __source: !0
          };
      t.createElement = function(e, t, r) {
        var o, a = {},
            i = null,
            c = null;
        if (null != t)
          for (o in void 0 !== t.ref && (c = t.ref), void 0 !== t.key &&
               (i = "" + t.key), t) y.call(t, o) && !v.hasOwnProperty(o) &&
            (a[o] = t[o]);
        var f = arguments.length - 2;
        if (1 === f) a.children = r;
        else if (1 < f) {
          for (var l = Array(f), s = 0; s < f; s++) l[s] = arguments[s + 2];
          a.children = l
        }
        if (e && e.defaultProps)
          for (o in f = e.defaultProps) void 0 === a[o] && (a[o] = f[
            o]);
        return {
          $$typeof: n,
          type: e,
          key: i,
          ref: c,
          props: a,
          _owner: h
        }
      }, t.forwardRef = function(e) {
        return {
          $$typeof: a,
          render: e
        }
      }
    },
    540: (e, t, r) => {
      e.exports = r(287)
    }
  },
      t = {};

  function r(o) {
    var n = t[o];
    if (void 0 !== n) return n.exports;
    var a = t[o] = {
      exports: {}
    };
    return e[o](a, a.exports, r), a.exports
  }(() => {
    var e = r(540);
    const t = e.forwardRef((function({
      title: t,
      titleId: r,
      ...o
    }, n) {
      return e.createElement("svg", Object.assign({
        xmlns: "http://www.w3.org/2000/svg",
        viewBox: "0 0 20 20",
        fill: "currentColor",
        "aria-hidden": "true",
        "data-slot": "icon",
        ref: n,
        "aria-labelledby": r
      }, o), t ? e.createElement("title", {
        id: r
      }, t) : null, e.createElement("path", {
        fillRule: "evenodd",
        d: "M5.75 2a.75.75 0 0 1 .75.75V4h7V2.75a.75.75 0 0 1 1.5 0V4h.25A2.75 2.75 0 0 1 18 6.75v8.5A2.75 2.75 0 0 1 15.25 18H4.75A2.75 2.75 0 0 1 2 15.25v-8.5A2.75 2.75 0 0 1 4.75 4H5V2.75A.75.75 0 0 1 5.75 2Zm-1 5.5c-.69 0-1.25.56-1.25 1.25v6.5c0 .69.56 1.25 1.25 1.25h10.5c.69 0 1.25-.56 1.25-1.25v-6.5c0-.69-.56-1.25-1.25-1.25H4.75Z",
        clipRule: "evenodd"
      }))
    }));
    console.log(t)
  })()
})();
```

</details>
