A beautiful CRUD APPLICATION, using Redux RTK Query, in getting requests from a j.son server, here we are able to use the Rtk query.

created a file for the apiSlice called apiSlice.js, where we made use of the createApi and fetchBaseQuery imported from reduxjs/toolkit/query/react"

in the createApi we have the following  as objects
 - reducerPath as key and 'api' as value

 - we have the baseQuery as key and 'fetchBaseQuery({baseUrl:"http:....})' we use this to fetch the data from the         json-server

 -tagTypes - An array of string tag type names. Specifying tag types is optional, but you should define them so that they can be used for caching and invalidation. When defining a tag type, you will be able to provide them with providesTags and invalidate them with invalidatesTags when configuring endpoints.

 -endpoints - in the endpoints we have the different functions, here we have the CRUD functions,
   -getTodo
   -addTodo
   -deleteTodo
   -updateTodo, all individual have objects like;
      - query: () => "/todos",
      - transformResponse: res => res.sort((a,b) => b.id - a.id) // to sort the list in a descending order
      - providesTags:['Todo]
        - we used the providesTags: ['Todos'],Used by query endpoints. Determines which 'tag' is attached to the cached data returned by the query. Expects an array of tag type strings, an array of objects of tag types with ids, or a function that returns such an array.

this was a beautiful built, take advantage of RTK query generated custom hooks and also the transformResponse, here we can be creative with the data we get or post to our api.... 

So in this App We can basically Read, Add, Update and Delete .. A full CRUD application.




