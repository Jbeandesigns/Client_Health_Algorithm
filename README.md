# **Client Health Intervention Algorithm**

An interactive decision-support tool for Client Success teams to identify and implement appropriate interventions when client health metrics fall into yellow or red status zones.

## **🎯 Purpose**

This algorithm helps Client Success teams:

* **Quickly identify** root causes for declining client health metrics  
* **Standardize** intervention approaches across the team  
* **Reduce response time** from problem identification to action  
* **Improve client retention** through proactive, data-driven interventions  
* **Track patterns** in client health issues across your portfolio

## **📊 Key Metrics Covered**

The algorithm addresses four critical client health metrics:

### **1\. Fill Rate**

* **Green**: \> 70%  
* **Yellow**: 40-70%  
* **Red**: \< 40%

**Root Causes Addressed**:

* Increase in posted shifts outpacing pro pool expansion  
* Low active professional pool  
* Low shift engagement per professional  
* Poor specialty/skill matching

### **2\. Facility Cancellation Rate**

* **Green**: Top quartile (\< 7%)  
* **Yellow**: Mid quartile (7-15%)  
* **Red**: Bottom quartile (\> 15%)

**Root Causes Addressed**:

* Overly aggressive shift posting  
* Filled with internal staff after posting  
* Reduced patient volume/caseload  
* Changed unit/department needs

### **3\. Professional Cancellation Rate**

* **Green**: \< 10%  
* **Yellow**: 10-15%  
* **Red**: \> 15%

**Root Causes Addressed**:

* Poor facility experience  
* Lack of clear expectations  
* Scheduling conflicts  
* Competing opportunities

### **4\. Professional Churn**

* **Green**: Top quartile  
* **Yellow**: 25-50th percentile  
* **Red**: Bottom quartile

**Root Causes Addressed**:

* Limited shift opportunities  
* Competitive pay issues  
* Poor facility experience  
* Changed location/availability

## **🚀 Features**

* **Interactive Metric Selection**: Click on any metric to begin the intervention process  
* **Root Cause Analysis**: Drill down into specific causes for each metric  
* **Dual Intervention Paths**:  
  * Client-facing interventions for collaborative implementation  
  * Internal considerations for team coordination  
* **Mobile Responsive**: Works on desktop, tablet, and mobile devices  
* **Easy Navigation**: Intuitive back/forward flow through the decision tree  
* **Built-in Deployment Guide**: Complete instructions for implementation

## **🛠 Technology Stack**

* **React 17+**: Frontend framework  
* **Tailwind CSS**: Styling and responsive design  
* **Modern JavaScript (ES6+)**: Component logic  
* **No external dependencies**: Self-contained application

## **📋 Prerequisites**

* Node.js 14+ and npm  
* Git (for version control)  
* GitHub account (for GitHub Pages deployment)  
* Basic knowledge of React/JavaScript (for customization)

## **🚀 Quick Start**

### **Option 1: GitHub Pages Deployment (Recommended)**

1. **Create a new React application**:  
    bash

```shell
npx create-react-app client-health-algorithm
cd client-health-algorithm
```

3. 

4. **Configure for GitHub Pages**:  
    bash

```shell
npm install --save gh-pages
```

6. 

7. **Update package.json**:  
    json

```json
{
  "homepage": "https://yourusername.github.io/client-health-algorithm",
  "scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
  }
}
```

9. 

10. **Replace src/App.js** with the Client Health Algorithm component code  
11. **Deploy**:  
     bash

```shell
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/client-health-algorithm.git
git push -u origin main
npm run deploy
```

13. 

14. **Configure GitHub Pages**:  
    * Go to repository Settings \> Pages  
    * Select "gh-pages" branch as source  
    * Save settings

Your algorithm will be live at: `https://yourusername.github.io/client-health-algorithm`

### **Option 2: Webflow iframe Embedding**

1. Complete GitHub Pages deployment (Option 1\)  
2. In Webflow, add an Embed element with:  
    html

```html
<iframe 
  src="https://yourusername.github.io/client-health-algorithm" 
  width="100%" 
  height="800px" 
  frameborder="0"
></iframe>
```

4. 

## **📁 Project Structure**

```
client-health-algorithm/
├── public/
│   ├── index.html
│   └── favicon.ico
├── src/
│   ├── App.js              # Main Client Health Algorithm component
│   ├── index.js            # React DOM rendering
│   └── index.css           # Additional styles
├── package.json            # Dependencies and scripts
└── README.md              # This file
```

## **🎨 Customization**

### **Adding New Metrics**

To add additional metrics, update the `metrics` object in `App.js`:

javascript

```javascript
const metrics = {
  // existing metrics...
  newMetric: {
    title: "New Metric Name",
    description: "Description of what this metric measures",
    thresholds: {
      red: "< X%",
      yellow: "X-Y%", 
      green: "> Y%"
    },
    rootCauses: [
      {
        id: "nm1",
        name: "Root cause description",
        clientInterventions: ["Intervention 1", "Intervention 2"],
        internalInterventions: ["Internal action 1", "Internal action 2"]
      }
    ]
  }
};
```

### **Modifying Interventions**

Update the `clientInterventions` and `internalInterventions` arrays for any root cause to customize the recommended actions.

### **Styling Changes**

The application uses Tailwind CSS classes. Modify the `className` attributes to change styling:

javascript

```javascript
<div className="bg-blue-500 text-white p-4 rounded-lg">
  // Your content
</div>
```

## **🔧 Maintenance**

### **Updating Content**

1. Make changes to the React component  
2. Test locally with `npm start`  
3. Deploy updates with `npm run deploy`

### **Version Control**

* Use semantic versioning (e.g., v1.0.0, v1.1.0, v2.0.0)  
* Tag releases: `git tag v1.0.0 && git push origin v1.0.0`  
* Keep a changelog of updates

### **Monitoring Usage**

Consider adding analytics to track:

* Which metrics are accessed most frequently  
* Most common root causes selected  
* User flow patterns through the algorithm

## **🔒 Security Considerations**

* **No sensitive data**: The algorithm contains only general intervention strategies  
* **Public repository**: Safe for public GitHub repositories  
* **No external API calls**: All logic runs client-side  
* **No user data collection**: Tool doesn't store or transmit user information

## **🌐 Browser Compatibility**

* Chrome 70+  
* Firefox 65+  
* Safari 12+  
* Edge 79+  
* Mobile browsers (iOS Safari, Chrome Mobile)

## **📱 Mobile Responsiveness**

The algorithm is fully responsive and works on:

* Desktop computers (1024px+)  
* Tablets (768px \- 1024px)  
* Mobile phones (320px \- 768px)

## **🆘 Troubleshooting**

### **Common Issues**

**Algorithm not displaying**:

* Check that React and dependencies are properly installed  
* Verify the homepage URL in package.json matches your GitHub Pages URL  
* Ensure the repository is public and GitHub Pages is enabled

**Styling issues**:

* Verify Tailwind CSS classes are loading correctly  
* Check for CSS conflicts if embedded in existing site  
* Test in different browsers to identify browser-specific issues

**Deployment failures**:

* Ensure gh-pages package is installed  
* Verify GitHub repository permissions  
* Check that the build process completes without errors

### **Getting Help**

1. **Check the built-in deployment guide** within the application  
2. **Review GitHub Pages documentation**: [https://pages.github.com/](https://pages.github.com/)  
3. **Contact your IT team** for organizational-specific deployment requirements  
4. **Consider alternative hosting**: Netlify, Vercel, or other static site hosts

## **📈 Future Enhancements**

Potential improvements for future versions:

* **Data Integration**: Connect to live client health dashboards  
* **Progress Tracking**: Track intervention implementation and results  
* **Custom Branding**: White-label options for different organizations  
* **Export Functionality**: Generate PDF intervention plans  
* **Analytics Dashboard**: Track algorithm usage and intervention effectiveness  
* **Multi-language Support**: Localization for global teams  
* **Integration APIs**: Connect with existing CRM or client management systems

## **🤝 Contributing**

To contribute improvements:

1. Fork the repository  
2. Create a feature branch: `git checkout -b feature-name`  
3. Make your changes and test thoroughly  
4. Commit with descriptive messages: `git commit -m "Add new metric for..."`  
5. Push to your branch: `git push origin feature-name`  
6. Create a Pull Request with detailed description

## **📄 License**

This project is intended for internal use within your organization. Modify the license as appropriate for your company's intellectual property policies.

## **📞 Support**

For technical support or questions about implementation:

* **Internal IT Team**: Contact your organization's IT department  
* **Developer Support**: Reach out to the development team that created this tool  
* **Documentation**: Refer to the built-in deployment guide and this README

## **📊 Data Sources**

This algorithm is based on:

* Client health metrics from CareRev's account review processes  
* Root cause analysis from actual client success interventions  
* Best practices from healthcare staffing industry  
* Intervention strategies proven effective in real client scenarios

---

**Last Updated**: January 2025  
 **Version**: 1.0.0  
 **Compatibility**: React 17+, Modern Browsers

