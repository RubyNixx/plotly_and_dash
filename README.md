# Plotly and Dash - Python (Datacamp session March 2025)

## Notes:

Dash is a Python framework for building interactive web applications. It combines Flask, Plotly.js, and React.js, allowing users to create dashboards without extensive knowledge of HTML, CSS, or JavaScript.

### Steps to Create a Basic Dash App:

1. **Install Dash**: Run `pip install dash` in your terminal.

2. **Set Up Your App**:
   - Import necessary libraries such as `Dash`, `html`, `dcc` (Dash Core Components), and Plotly for visualizations.
   - Initialize the app using `app = Dash()`.

3. **Define Layout**:
   - Use Dash components like `html.Div`, `dcc.Graph`, and `dash_table.DataTable` to structure your app.
   - Example layout:

     ```
     app.layout = html.Div([
         html.H1("My Dashboard"),
         dcc.Graph(figure=px.histogram(df, x='continent', y='lifeExp', histfunc='avg')),
         dash_table.DataTable(data=df.to_dict('records'), page_size=10)
     ])
     ```

4. **Add Interactivity**:
   - Define callbacks using `@app.callback` to update components dynamically based on user inputs.

5. **Run Your App**:
   - Use `app.run_server(debug=True)` to start the server locally.

For a detailed tutorial, refer to the official Dash documentation.

## Hosting a Dash Dashboard

### Free Hosting Options

1. **PythonAnywhere**:
   - Allows free deployment of one web app, including Dash dashboards.
   - Steps:
     1. Create an account on PythonAnywhere.
     2. Upload your app files.
     3. Configure the web app settings (e.g., WSGI file pointing to your Dash app).
     4. Access your dashboard via the provided URL.

2. **Render**:
   - Offers a free tier for hosting web apps.
   - Deploy Dash apps by uploading your project repository and configuring the environment.

3. **Cloud Run (Google)**:
   - Has a free tier for deploying containerized applications.
   - Package your Dash app into a Docker container and deploy it on Cloud Run.

### Paid Hosting Options

1. **Dash Enterprise**:
   - Provides robust tools for deploying, scaling, and securing your dashboards.
   - Install the Dash Enterprise CLI, log in, and use the command `de deploy <path> --name <app-name>` to deploy your app.

2. **Local Server**:
   - Host the app on a local server using `app.run_server(host='0.0.0.0')`. This allows external access within the same network via your IP address (e.g., `192.168.x.x:8050`).

Choose the hosting method based on your budget and requirements!

### Shaffer's 4Cs:

- Clear
- Clean
- Concise
- Captivating

### Dash app code:

![image](https://github.com/user-attachments/assets/ab55daed-6af4-41e5-808c-7f4c542e6db5)

## Resources

### YouTube Video:
[Building Dashboards with Plotly and Dash](https://www.youtube.com/watch?v=PVOxoNWjJEA)

### Code Editor:
[Plotly code editor - wasmdash](https://wasmdash.vercel.app/)

### Cheat Sheet:
[Plotly Express Cheat Sheet](https://www.datacamp.com/cheat-sheet/plotly-express-cheat-sheet)

### Code for each chart:
- [Plotly Python Documentation & Code](https://plotly.com/python/)
- [Plotly GitHub](https://github.com/plotly/plotly.py)

### Tutorials:
- [Map creation in python using plotly](https://www.datacamp.com/tutorial/making-map-in-python-using-plotly-library-guide)
- [Python Plotly Express Tutorial: Unlock Beautiful Visualizations](https://www.datacamp.com/tutorial/python-plotly-express-tutorial)

### Checklist for designing dashboards:
[Datacamp Infographic Dashboard Design Checklist](https://www.datacamp.com/blog/infographic-dashboard-design-checklist)

### Examples of Dashboards built in Plotly Community:
- [Michelin Star Restaurants - Dash apps](https://community.plotly.com/t/autumn-app-challenge/87373/9)
- [Data Visualization & Dashboards](https://plotly.com/examples/dashboards/)
- [Plotly Figure Friday](https://community.plotly.com/t/announcing-plotly-weekly-data-viz-projects-figure-friday/84953)
