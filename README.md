# dicoding_part_1

## How to run the application:

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## Explanation of my search solution

I have imported the JSON file given to me into the src/components folder. I then import them into my DicodingApp.vue file where I will request for a search from the user. The information will then be parsed through the filteredCourses function which will return courses which title/summary/description are relevant to the search query regardless of case sensitivity. The information will then go back to the HTML template which shows the relevant data (name, description and link).