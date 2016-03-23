# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
  Loading the appropriate model is one job inside Application Router. Router also manage manage your application URL.
  We use the Router for the core flow of your app which deals with URLs .
  When your application starts, the router is responsible for displaying templates, loading data, and otherwise setting up application state. It does so by matching the current URL to the routes that you've defined.

  one of the two big responsibilities of the Route is to parse the URL and extract meaningful information - dynamic segments are the primary instance of this.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to 'campus.boston'}}Boston{{/link-to}}

    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here

    ```

    ```md
      The first one is a nested route
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    router will create params ID. get a product w/ params.<name>_id
    params: 
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
  You use {{outlet}}.
    ```
