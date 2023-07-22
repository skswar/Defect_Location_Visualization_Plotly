<div align="center">
<img src="https://raw.githubusercontent.com/skswar/Manufacturing_Defect_Analysis_and_Visualization/master/img/banner.png" alt="Intro Logo" width="90%"></div>
<h3 align="center">How can we analyze Defects to Improve Product Quality?</h3>
<br/>

## Table of contents
* [Introduction](#introduction)
* [Methodology](#methodology)
  * [Understanding Product Dimensions](#understanding-product-dimensions)
  * [Highlighting Pain Points](#highlighting-pain-points)
* [Conclusion](#conclusion)

<hr>

## Introduction
In any industry, understanding and improving product quality are of utmost importance. Not only does it enhance customer trust, but it also reduces production costs, contributing to overall profitability. This project aims to explore product quality rejection data in detail and analyze the reasons for product rejections. By taking proactive actions based on these insights, we can effectively enhance the overall manufacturing process.

The products that I am analyzing in this project is called Instrument Protectors (the link of the products has been mentioned below). The data is gathered by a computer vision system which captures the image of a product, processes it, identifies a defect and logs the region of the defect's coordinates (x,y regions). The idea is to thoroughly examine these defect logs, identify critical regions, and present the findings in a clear and actionable manner to highlight potential issues in the product.

<u>Product Link</u>: 
1. [Small Card](http://www.globalindustrial.com/p/attest-instrument-protectors-13911-2-inch-x-5-inch-100-each-pack-10-packs-case)
2. [Medium Card](http://www.globalindustrial.com/p/attest-instrument-protectors-13913-3-1-2-inch-x-6-5-8-inch-100-each-pack-10-packs-case)

## Methodology
To achieve the goal, I initially examined the defect logs data and visualized the defect coordinates. Subsequently, I attempted to create a plot to highlight the critical defect regions. However, as I delved deeper into the analysis, I quickly realized that the task was not as straightforward as anticipated.

### Understanding Product Dimensions
In this project we are analyzing two similar products but of different dimensions. Thus the defect coordinates are going to vary based on the product size. Although we are unknown about the original dimensions of the product but by analyzing the below two plots (Fig. 1) we can clearly have an idea how to segregate the two products based on their defect regions. It also very difficult to say at this moment which are the most critical area of issue for the product as the defect is occuring throughout. 

For the smaller product, a rectangular region is clearly visible whereas for the medium sized product a rectangular white line can be identified in between by a close look. It is important to notice that any time a defect coordinate is getting logged out of this rectangular regions are happening becuase of misaalignment. Therefore it also will be important to note the number of products being rejected due to misallignment. From the below plot though, it is very clear that medium sized products are having a lot more misallignment than the small products.

<p align="center">
<img src="https://raw.githubusercontent.com/skswar/Manufacturing_Defect_Analysis_and_Visualization/master/img/loc_small.PNG" width="300px" height="250px"/>
<img src="https://raw.githubusercontent.com/skswar/Manufacturing_Defect_Analysis_and_Visualization/master/img/loc_med.PNG" width="350px" height="250px"/><p align="center">Fig. 1</p>
</p>




**Link to Notebook with plotly graphs**: [Defect_Location_Visualization.ipynb](https://nbviewer.org/github/skswar/Manufacturing_Defect_Analysis_and_Visualization/blob/main/python_scripts/Defect_Location_Visualization.ipynb)


