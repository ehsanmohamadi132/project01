dt2 = df.query("`World Rank` <100" )
dt2['Institution']
location_counts = dt2['Location'].value_counts()
plt.figure(figsize=(8, 8))
plt.pie(location_counts, labels=location_counts.index, autopct='%1.0f%%', startangle=140)
plt.title('Distribution of Locations with World Rank > 950 and National Rank < 10')
plt.savefig('p2.jpg')
plt.show()
