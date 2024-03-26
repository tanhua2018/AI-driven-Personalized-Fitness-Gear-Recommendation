# AI-driven-Personalized-Fitness-Gear-Recommendation
Entwickeln Sie ein KI-gesteuertes System, das auf der Grundlage von Körpertyp, Fitnessniveau und Trainingszielen personalisierte Empfehlungen für Fitnessgeräte und -ausrüstung gibt.
class FitnessGearRecommender:
    def __init__(self):
        self.gear_recommendations = {
            'weight_loss': {
                'beginner': ['Jump rope', 'Yoga mat'],
                'intermediate': ['Kettlebell', 'Resistance bands'],
                'advanced': ['Adjustable dumbbells', 'Pull-up bar']
            },
            'muscle_gain': {
                'beginner': ['Resistance bands', 'Dumbbells'],
                'intermediate': ['Kettlebell', 'Weighted vest'],
                'advanced': ['Barbell set', 'Bench press']
            },
            'flexibility': {
                'beginner': ['Yoga mat', 'Foam roller'],
                'intermediate': ['Balance ball', 'Stretching straps'],
                'advanced': ['Pilates reformer', 'Mobility bands']
            }
        }

    def get_recommendations(self, body_type, fitness_level, goal):
        # This is a simplified logic. Real implementation would involve more complex decision making
        # and potentially a machine learning model for personalization.
        try:
            recommendations = self.gear_recommendations[goal][fitness_level]
            print(f"Based on your body type: {body_type}, fitness level: {fitness_level}, and goal: {goal},")
            print("we recommend the following fitness gear for you:")
            for gear in recommendations:
                print(f"- {gear}")
        except KeyError:
            print("Sorry, we couldn't find recommendations for your specific criteria.")

if __name__ == "__main__":
    body_type = input("Enter your body type (e.g., ectomorph, mesomorph, endomorph): ").lower()
    fitness_level = input("Enter your fitness level (beginner, intermediate, advanced): ").lower()
    goal = input("Enter your training goal (weight_loss, muscle_gain, flexibility): ").lower()

    recommender = FitnessGearRecommender()
    recommender.get_recommendations(body_type, fitness_level, goal)
