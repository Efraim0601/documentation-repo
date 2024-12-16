- The term 'content management' generally refers to a system for acquiring, storing and retrieving electronic data in varying formats - such as text, images or proprietary formats.
- Content management systems (CMS) usually incorporate a rendering system to let the developer display the content in various formats.
- While some CMSs are rigid in the manner in which content is entered and rendered, the content management module of APOGEE is more of a set of tools which can be used in a variety of situations.
- In addition to HTML, the content can be rendered in non-Web modes, such as PDF or email newsletters.
- The APOGEE CMS is designed to store data once and then allow it to be reused in multiple arrangements.
- Hence, there are basically two aspects
- <ul>
      <li>the back-end storage subsystem, which is oriented around the DataResource entity</li>
      <li>the front-end association subsystem, which revolves around the Content entity</li>
  </ul>
- Note that the Content entity has a foreign key pointing to one and only one DataResource entity, but the same DataResource entity can be referenced by multiple Content entities.
- It is a general rule that data can only be accessed via a Content entity, but one common exception is that images are typically served up using the DataResource primary key.
- Content entities are related to other content via ContentAssoc entities. The ContentAssoc entity has a four part primary key and other fields that are used to relate content. The key specifies the 'to' Content and the 'from' Content, as well as the type of association and its effective date. See the discussion of the ContentAssoc entity for more information on how content is related.