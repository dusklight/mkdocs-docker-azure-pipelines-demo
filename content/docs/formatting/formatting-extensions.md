# Formatting Samples - Extensions

Demo of MkDocs with extensions formatting.  See all extension formatting examples at [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/extensions/admonition/)

## Admonition

!!! note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.


## CodeHilite Syntax Highlighting

```bash
    test.yml    # comment 1
    script.sh   # comment 2
```

```c#
  /// <summary>
  /// Initializes a new instance of the DefaultHttpContext class with options passed in.
  /// </summary>
  /// <param name="featureCollection">Options to set when instantianting the Default HTTP context object.</param>
  public HttpContext Create(IFeatureCollection featureCollection)
  {
      if (featureCollection == null)
      {
          throw new ArgumentNullException(nameof(featureCollection));
      }

      var httpContext = new DefaultHttpContext(featureCollection);
      if (_httpContextAccessor != null)
      {
          _httpContextAccessor.HttpContext = httpContext;
      }

      httpContext.FormOptions = _formOptions;
      httpContext.ServiceScopeFactory = _serviceScopeFactory;

      return httpContext;
  }
```

Inline code syntax highlighting: `#!js function pad(v){return ('0'+v).split('').reverse().splice(0,2).reverse().join('')}`.

## Tasklist

* [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
* [x] Nulla lobortis egestas semper
* [x] Curabitur elit nibh, euismod et ullamcorper at, iaculis feugiat est
* [ ] Vestibulum convallis sit amet nisi a tincidunt
    * [x] In hac habitasse platea dictumst
    * [x] In scelerisque nibh non dolor mollis congue sed et metus
    * [x] Sed egestas felis quis elit dapibus, ac aliquet turpis mattis
    * [ ] Praesent sed risus massa
* [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque
* [ ] Nulla vel eros venenatis, imperdiet enim id, faucibus nisi

