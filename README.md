

# Flask Project with WTFORMS

wprking with flask and wtforms to create validations and csfr-hash keys, below
is a snippet of the code.  and how the fields work with DataRequired and creating
choices using Tupels in dictionaries

``` python
class infoForm(FlaskForm):
    breed = StringField("what Breed are you?", validators=[DataRequired()])
    neuter = BooleanField('have you been Neutered')
    mood = RadioField('Please chose your moode', choices=[
        ('mood_1', 'Happy'), ('mood_two', 'Excited')])
    food_choice = SelectField(u'Pick your favorite food:', choices=[
        ('chi', 'Chicken'), ('bf', 'beef'), ('fish', 'Fish')])
    feedback = TextAreaField()
    submit = SubmitField('Submit')
