# product-management-foundry

// Logic Model Data Object
const logicModel = {
  inputs: [
    { id: 1, name: "Donations", description: "Amount of money donated" },
    { id: 2, name: "Volunteers", description: "Number of volunteers" },
    { id: 3, name: "Programs", description: "Number of programs offered" },
  ],
  activities: [
    { id: 1, name: "Fundraising events", description: "Organizing events to raise funds" },
    { id: 2, name: "Volunteer training", description: "Providing training to volunteers" },
    { id: 3, name: "Program development", description: "Developing new programs to meet needs" },
  ],
  outputs: [
    { id: 1, name: "Funds raised", description: "Amount of money raised from donations" },
    { id: 2, name: "Volunteer hours", description: "Number of hours volunteered" },
    { id: 3, name: "Program participants", description: "Number of people participating in programs" },
  ],
  outcomes: [
    { id: 1, name: "Increased awareness", description: "More people are aware of the organization's mission" },
    { id: 2, name: "Improved quality of life", description: "People's lives are improved through the organization's programs" },
    { id: 3, name: "Increased sustainability", description: "The organization is able to sustain its activities and growth" },
  ],
};

// User Persona Data Object
const userPersonas = [
  {
    id: 1,
    name: "Samantha",
    age: 35,
    gender: "Female",
    interests: "Social justice, education",
    needs: "Easy ways to donate, volunteer opportunities",
    painPoints: "Limited time, financial constraints",
  },
  {
    id: 2,
    name: "John",
    age: 50,
    gender: "Male",
    interests: "Healthcare, community service",
    needs: "Ways to get involved, impact measurement",
    painPoints: "Lack of trust in nonprofits, limited resources",
  },
];

// Jobs-to-be-Done Data Object
const jobsToBeDone = [
  {
    personaId: 1,
    functionalGoal: "Donate money to support the cause",
    socialGoal: "Show support for the organization and its mission",
    emotionalGoal: "Feel good about contributing to a worthy cause",
  },
  {
    personaId: 2,
    functionalGoal: "Find volunteer opportunities in the community",
    socialGoal: "Connect with other like-minded people and make a difference",
    emotionalGoal: "Feel fulfilled and make a positive impact on others",
  },
];

// User Journey Maps Data Object
const userJourneyMaps = [
  {
    personaId: 1,
    stages: [
      {
        name: "Awareness",
        touchpoints: [
          { id: 1, name: "Social media post", description: "Sees a post about the organization on social media" },
          { id: 2, name: "Word of mouth", description: "Hears about the organization from a friend or family member" },
        ],
        emotionalStates: [
          { id: 1, name: "Curiosity", description: "Wants to learn more about the organization" },


import React from 'react';
import { makeStyles } from '@material-ui/core/styles';
import { Typography, TextField, Checkbox, FormControlLabel, Select, MenuItem, Button, AppBar, Toolbar, IconButton, Drawer, List, ListItem, ListItemText } from '@material-ui/core';
import MenuIcon from '@material-ui/icons/Menu';

const drawerWidth = 240;

const useStyles = makeStyles((theme) => ({
  root: {
    display: 'flex',
  },
  appBar: {
    zIndex: theme.zIndex.drawer + 1,
  },
  menuButton: {
    marginRight: theme.spacing(2),
  },
  drawer: {
    width: drawerWidth,
    flexShrink: 0,
  },
  drawerPaper: {
    width: drawerWidth,
  },
  drawerContainer: {
    overflow: 'auto',
  },
  content: {
    flexGrow: 1,
    padding: theme.spacing(3),
  },
  form: {
    display: 'flex',
    flexDirection: 'column',
    maxWidth: '500px',
    margin: '0 auto',
    '& > *': {
      margin: theme.spacing(1),
    },
  },
  button: {
    alignSelf: 'flex-end',
  },
}));

function App() {
  const classes = useStyles();
  const [open, setOpen] = React.useState(false);

  const handleDrawerOpen = () => {
    setOpen(true);
  };

  const handleDrawerClose = () => {
    setOpen(false);
  };

  return (
    <div className={classes.root}>
      <AppBar position="fixed" className={classes.appBar}>
        <Toolbar>
          <IconButton
            edge="start"
            className={classes.menuButton}
            color="inherit"
            aria-label="menu"
            onClick={handleDrawerOpen}
          >
            <MenuIcon />
          </IconButton>
          <Typography variant="h6" noWrap>
            My Nonprofit App
          </Typography>
        </Toolbar>
      </AppBar>
      <Drawer
        className={classes.drawer}
        variant="temporary"
        anchor="left"
        open={open}
        onClose={handleDrawerClose}
        classes={{
          paper: classes.drawerPaper,
        }}
      >
        <div className={classes.drawerContainer}>
          <List>
            <ListItem button>
              <ListItemText primary="Home" />
            </ListItem>
            <ListItem button>
              <ListItemText primary="About" />
            </ListItem>
            <ListItem button>
              <ListItemText primary="Contact" />
            </ListItem>
          </List>
        </div>
      </Drawer>
      <main className={classes.content}>
        <Typography variant="h4" gutterBottom>
          Logic Model
        </Typography>
        <Typography variant="body1" gutterBottom>
          Here's where you can input your nonprofit's logic model information.
        </Typography>
        <form className={classes.form}>
          <TextField id="name" label="Name" variant="outlined" />
          <TextField id="email" label="Email" variant="outlined" type="email" />
          <TextField id="password" label="Password" variant="outlined" type="password" />
          <FormControlLabel
            control={<Checkbox id="remember-me" />}
            label="Remember me"
          />
          <Select
            labelId="job-to-be-done"
            id="job-to-be-done"
            value=""
            variant="outlined"
          >
            <MenuItem value="">
              <em>Select a job to be done</em>
            </MenuItem>
            <MenuItem value={10}>Job 1</MenuItem>
            <MenuItem value

import React from 'react';
import { makeStyles } from '@material-ui/core/styles';
import { Typography, TextField, Checkbox, FormControlLabel, Select, MenuItem, Button, AppBar, Toolbar, IconButton, Drawer, List, ListItem, ListItemText } from '@material-ui/core';
import MenuIcon from '@material-ui/icons/Menu';

const drawerWidth = 240;

const useStyles = makeStyles((theme) => ({
  root: {
    display: 'flex',
  },
  appBar: {
    zIndex: theme.zIndex.drawer + 1,
  },
  menuButton: {
    marginRight: theme.spacing(2),
  },
  drawer: {
    width: drawerWidth,
    flexShrink: 0,
  },
  drawerPaper: {
    width: drawerWidth,
  },
  drawerContainer: {
    overflow: 'auto',
  },
  content: {
    flexGrow: 1,
    padding: theme.spacing(3),
  },
  form: {
    display: 'flex',
    flexDirection: 'column',
    maxWidth: '500px',
    margin: '0 auto',
    '& > *': {
      margin: theme.spacing(1),
    },
  },
  button: {
    alignSelf: 'flex-end',
  },
  svg: {
    maxWidth: '100%',
    height: 'auto',
  },
}));

function LogicModel() {
  const classes = useStyles();

  return (
    <div>
      <Typography variant="h4" gutterBottom>
        Logic Model
      </Typography>
      <Typography variant="body1" gutterBottom>
        Here's where you can input your nonprofit's logic model information.
      </Typography>
      <form className={classes.form}>
        <TextField id="name" label="Name" variant="outlined" />
        <TextField id="email" label="Email" variant="outlined" type="email" />
        <TextField id="password" label="Password" variant="outlined" type="password" />
        <FormControlLabel
          control={<Checkbox id="remember-me" />}
          label="Remember me"
        />
        <Select
          labelId="job-to-be-done"
          id="job-to-be-done"
          value=""
          variant="outlined"
        >
          <MenuItem value="">
            <em>Select a job to be done</em>
          </MenuItem>
          <MenuItem value={10}>Job 1</MenuItem>
          <MenuItem value={20}>Job 2</MenuItem>
          <MenuItem value={30}>Job 3</MenuItem>
        </Select>
        <Button variant="contained" color="primary" className={classes.button}>
          Submit
        </Button>
      </form>
    </div>
  );
}

function UserPersonas() {
  const classes = useStyles();

  return (
    <div>
      <Typography variant="h4" gutterBottom>
        User Personas
      </Typography>
      <Typography variant="body1" gutterBottom>
        Here's where you can input information about your nonprofit's user personas.
      </Typography>
      <form className={classes.form}>
        <TextField id="name" label="Name" variant="outlined" />
        <Select
          labelId="persona-type"
          id="persona-type"
          value=""
          variant="outlined"
        >
          <MenuItem value="">
            <em>Select a persona type
