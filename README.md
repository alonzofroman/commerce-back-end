# E-Commerce Back-End

## Author
Alonzo Roman

## Table of Contents
* [Summary](#Summary)
* [Code](#Code)
* [Install](#Install)
* [Video](#Video)
* [Technologies](#Technologies)
* [Contact](#Contact-Links)

## Summary
The purpose of this project is to create a a back-end for an e-commerce website. It is possible for users to utilize this program with Insomnia in order to view categories, products, and tags, as well as add, delete, and update them within the MySQL database. 

## Code Snippet
The use of express and mysql were used to create commands following GET requests to the database. In the following example, a route is created to handle retrieving all category table data from the database. It utilizes an async function and logs either the category data from the database upon success, and the error code in the result of an error. 

```Javascript
router.get('/', async (req, res) => {
  try {
    const categoryData = await Category.findAll({
      include: [{ model: Product }]
    });
    res.status(200).json(categoryData);
  } catch (err) {
    res.status(500).json(err);
  }
});
```

## Install
- Clone down the repository
- Change env.EXAMPLE to use your mySQL username and password, rename .env
- Use npm install in repository through your terminal
- Use npm run seed if you wish to use test seeds
- Use npm start to begin the program
- Utilize Insomnia to make requests to localhost:3001

## Video
- [Video](https://watch.screencastify.com/v/aTfi6Knn1E1yVwgeetTP)

## Technologies

- [Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Node.js](https://nodejs.org/en/docs/)
- [Express](https://expressjs.com/)
- [mySQL](https://dev.mysql.com/doc/)
- [Sequelize](https://sequelize.org/)
- [Dotenv](https://www.npmjs.com/package/dotenv)
- [Insomnia](https://docs.insomnia.rest/)



## Contact Links

- [Github](https://github.com/alonzofroman)
- [LinkedIn](https://www.linkedin.com/in/alonzo-roman/")

## Resources/Acknowledgements 

- [W3Schools](https://www.w3schools.com/)
- [MDN Web Docs](https://developer.mozilla.org/en-US/)