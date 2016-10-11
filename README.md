# reactContainerComponents

<img src="https://cloud.githubusercontent.com/assets/19864300/19284781/ca356f6a-9053-11e6-925b-98c65935395d.png" />

#separating presentational components from display components.

<GuineaPigs />'s job is to render a photo carousel of guinea pigs. It does this perfectly well! And yet, it has a problem: it does too much stuff.

We can break <GuineaPigs /> into smaller components, but before we do: how do we know that GuineaPigs does too much stuff? How can you tell when a component has too many responsibilities?

Separating container components from presentational components helps to answer that question. It shows you when it might be a good time to divide a component into smaller components. It also shows you how to perform that division.

Separating container components from presentational components is a popular React programming pattern.

Here's the basic idea behind it: if a component has to have state, make calculations based on props, or manage any other complex logic, then that component shouldn't also have to render HTML-like JSX.

Instead of rendering HTML-like JSX, the component should render another component. It should be that component's job to render HTML-like JSX.

Following this pattern separates your business logic from your presentational logic, which is a Good Thing.

GuineaPigs.js contains a lot of logic! You can't even see the render function unless you scroll down.

It makes sense that GuineaPigs would have so much work to do. It has to select the correct guinea pig to render, wait the right amount of time before rendering, render an image, select the next correct guinea pig, and so on.

Let's divide GuineaPigs in a presentational component and a container component.

Create a new file named GuineaPigsContainer.js and divide GuineaPigs into two separate component classes: GuineaPigs and GuineaPigsContainer.

In this programming pattern, the container component does the work of figuring out what to display. The presentational component does the work of actually displaying it. If a component does a significant amount of work in both areas, then that's a sign that you should use this pattern!

You can find a lot of intelligent articles written about this pattern. Here's a nice one to start with. https://medium.com/@learnreact/container-components-c0e67432e005#.gacsoomn1
