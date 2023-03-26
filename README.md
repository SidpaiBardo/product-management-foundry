# product-management-foundry

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
