# Iterating

<%= partial("docs/disclaimer.html") %>

<%= title("Iterating Through Arrays", {name: "each-array"}) %>

When looping through `arrays` or `slices`, the block being looped through will have access to the "global" context.

The `for` statement takes 1 - 2 arguments. When using the two argument version, the first argument is the "index" of the loop and the second argument is the value from the array or slice.

<%= code("html") { %>
<ul>
  \\<%= for (index, name) in names { %>
    <li>\\<%= index %> - \\<%= name %></li>
  \\<% } %>
</ul>
<% } %>

When using the one argument version the index is omitted and just the value is returned:

<%= code("html") { %>
<ul>
  \\<%= for (name) in names { %>
    <li>\\<%= name %></li>
  \\<% } %>
</ul>
<% } %>

<%= title("Iterating Through Maps", {name:"each-maps"}) %>

Looping through `maps` using the `each` helper is also supported, and follows very similar guidelines to looping through `arrays`.

When using the two argument version, the first argument is the key of the map and the second argument is the value from the map:

<%= code("html") { %>
<ul>
  \\<%= for (key, value) in users { %>
    <li>\\<%= key %> - \\<%= value %></li>
  \\<% } %>
</ul>
<% } %>

When using the one argument version the key is omitted and just the value is returned:

<%= code("html") { %>
<ul>
  \\<%= for (user) in users { %>
    <li>\\<%= user %></li>
  \\<% } %>
</ul>
<% } %>
