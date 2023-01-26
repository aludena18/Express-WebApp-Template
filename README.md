"use strict";

import mongoose from "mongoose";
import express from "express";
import \_ from "lodash";

const MONGO_URL = "mongodb://127.0.0.1:27017";
const DATABASE_NAME = "blogDB";

const app = express();
app.set("view engine", "ejs");
app.use(express.urlencoded({ extended: true }));
app.use(express.static("public"));

mongoose.set("strictQuery", false);
mongoose.connect(`${MONGO_URL}/${DATABASE_NAME}`);

// GET Methods
app.get("/", (req, res) => {});

// POST Methods
app.post("/", (req, res) => {});

// Start server
app.listen(process.env.PORT || 3000, function () {
console.log("Server Running!");
});
