- To follow this topic, click on the 'Catalog Detail List' in the left-hand panel under the 'Browse Catalogs' section.
  Then click on any catalog in the table of current catalogs presented in the main screen.
- You will see the top-level editing screen for that catalog.
  Along the top of the working screen are four sub-tabs: Catalog, Stores, Parties and Catalogs.
  Each of those are discussed as a topic below.
-
- ### Catalog tab
  The main Catalog tab for a product catalog is mostly for establishing the look and feel.
  
  Each catalog can have its own style sheet (CSS), its own logo, and its own content repository (the content path prefix) and templates prefix (where its freemarker templates are located).
- ### The Stores tab
- The 'Stores' tab shows a list of Stores that this Catalog is currently featured in.
- #+BEGIN_IMPORTANT
  Stores and Catalogs do not have a one-to-one relationship: the same Store can feature multiple Catalogs, and the same Catalog could be featured in many Stores.
  #+END_IMPORTANT
- ### The Parties tab
- Here you identify which Party is responsible for or assigned to work with the specific Catalog selected.
- The Party’s Role is assigned or identified and, if appropriate, a start and/or finish date for the assignment can be specified.
-
- ### Categories tab
- The 'categories' tab shows the different product categories and their roles for this catalog. Specifically:
	- <ul>
	  <li>Each catalog can (should) have a 'Browse Root' category, which is used as the root category for navigation. </li>For example, the navigation menu would start at this category and show its child categories.
	  <li>Each catalog can also have a 'Promotions' category, which is shown first to the customer when he signs in to the site.</li>
	  <li>There is also a 'Default Search' category. Products in this category are used for search results first.</li>
	  <li>'Quick add' categories are used to specify categories where products can be added in bulk to the cart from the same screen.</li>
	  </ul>
-