icon:: 🗒️

- query-properties:: [:page]
  #+BEGIN_QUERY
  {:title "List" :query [:find (pull ?p [*]) :where [?p :block/name _] [?p :block/properties ?props] [(get ?props :type) ?val] [(= ?val "Quick Note")]]}
  #+END_QUERY