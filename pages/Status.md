icon:: ⏺️

- # Concept
  query-properties:: [:page :type :tags]
  query-sort-by:: page
  query-sort-desc:: false
  #+BEGIN_QUERY
  {:title "List" :query [:find (pull ?p [*]) :where [?p :block/name _] [?p :block/properties ?props] [(get ?props :status) ?val] [(= ?val "Concept")]]}
  #+END_QUERY
- # In Development
  query-properties:: [:page :type :tags]
  #+BEGIN_QUERY
  {:title "List" :query [:find (pull ?p [*]) :where [?p :block/name _] [?p :block/properties ?props] [(get ?props :status) ?val] [(= ?val "In Development")]]}
  #+END_QUERY
- # Finished
  query-properties:: [:page :type :tags]
  #+BEGIN_QUERY
  {:title "List" :query [:find (pull ?p [*]) :where [?p :block/name _] [?p :block/properties ?props] [(get ?props :status) ?val] [(= ?val "Finished")]]}
  #+END_QUERY
-