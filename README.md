# Function to perform linear extrapolation
perform_extrapolation <- function(x, y, new_x) {
  # Fit a linear regression model
  model <- lm(y ~ x)
  
  # Use the model to predict new values based on new_x
  predicted_y <- predict(model, newdata = data.frame(x = new_x))
  
  # Display the linear model coefficients
  cat("Linear model coefficients:\n")
  print(coef(model))
  
  # Display the extrapolated values
  cat("\nExtrapolated values for new_x:", new_x, "\n")
  print(predicted_y)
}
